# LeadPulse Platform Data Model

This document defines the core database architecture for the LeadPulse SaaS platform.

LeadPulse uses a **multi-tenant database model** built on Supabase (PostgreSQL).

The system must ensure:

• tenant isolation  
• scalable campaign tracking  
• efficient analytics queries  
• secure data access  

---

# Multi-Tenant Architecture

Each organization using LeadPulse is a tenant.

Tenant types:

publisher  
advertiser  
agency  

All platform data must be associated with a tenant.

Key rule:

Every major table must include:

tenant_id

This ensures data isolation.

---

# Core Database Tables

The platform contains several core entities.

tenants  
users  
campaigns  
qr_scans  
leads  
landing_pages  
analytics_events  

---

# Tenants Table

Stores organizations using the platform.

Fields:

id (uuid primary key)

organization_name

organization_type

Values:

publisher  
advertiser  
agency  

created_at

Example:

id: 123  
organization_name: Real Estate Magazine  
organization_type: publisher

---

# Users Table

Users belong to a tenant.

Fields:

id (uuid)

tenant_id

email

role

Possible roles:

admin  
publisher_user  
advertiser_user  
agency_user  

created_at

---

# Campaigns Table

Campaigns represent advertising initiatives.

Fields:

id (uuid)

tenant_id

publisher_id

advertiser_id

campaign_name

industry

location

status

Values:

draft  
active  
paused  
completed  

created_at

---

# QR Codes

Each campaign has a dynamic QR code.

QR URL format:

/c/{campaignID}

QR data stored in campaigns table:

qr_code_url

---

# QR Scans Table

Records every QR scan.

Fields:

id (uuid)

campaign_id

tenant_id

timestamp

device_type

referrer

geo_country

geo_city

ip_hash

Purpose:

Track offline ad engagement.

---

# Landing Pages Table

Stores AI generated landing pages.

Fields:

id (uuid)

campaign_id

headline

subheadline

offer_description

cta_text

created_at

Landing pages must be lightweight.

---

# Leads Table

Stores captured leads.

Fields:

id (uuid)

campaign_id

tenant_id

name

phone

email

created_at

Future fields:

lead_score  
conversion_status  

---

# Analytics Events Table

Optional advanced analytics tracking.

Fields:

id (uuid)

campaign_id

event_type

timestamp

Possible events:

landing_view  
form_submit  
cta_click  

---

# Relationships

tenant

→ users  
→ campaigns  
→ leads  

campaign

→ qr_scans  
→ landing_pages  
→ leads  

---

# Indexing Strategy

Indexes required for performance:

campaign_id index on qr_scans

campaign_id index on leads

tenant_id index on campaigns

These indexes improve analytics queries.

---

# Data Security

Supabase row-level security must be enabled.

Policies must ensure:

users can only access data belonging to their tenant.

Example rule:

tenant_id must match authenticated user tenant.

---

# Scalability

The schema must support:

millions of QR scans

millions of leads

thousands of campaigns

Preferred query patterns:

campaign-based analytics  
tenant-based analytics  

Avoid full table scans.

---

# Future Extensions

Future tables may include:

publisher_inventory

ad_slots

lead_scoring

ai_optimization_logs

These tables must follow the same multi-tenant architecture.

---

# Final Principle

All platform data must always be associated with:

tenant_id

This ensures secure multi-tenant SaaS architecture.