# LeadPulse SaaS Starter Kit

This document defines the minimal code structure required for the LeadPulse MVP.

Claude must use this structure when initializing the platform.

---

# Technology Stack

Frontend:

Next.js
React
TailwindCSS

Backend:

Supabase
PostgreSQL

Hosting:

Vercel

---

# Initial Project Structure

leadpulse/

app/
dashboard/
campaigns/
landing/

components/

lib/

api/

qr/

database/

---

# Core Pages

/login

/dashboard

/campaigns

/campaign/{id}

/l/{campaignID}

---

# Core Components

AppLayout  
CampaignCard  
QRGenerator  
LeadForm  
AnalyticsCard  

---

# Database Tables

tenants  
users  
campaigns  
qr_scans  
leads  

---

# Campaign Flow

User creates campaign

↓

QR code generated

↓

QR scan logged

↓

Landing page displayed

↓

Lead captured

↓

Analytics updated

---

# Required Routes

Dashboard

/dashboard

Campaign creation

/campaigns/new

Landing page

/l/{campaignID}

QR redirect

/c/{campaignID}

---

# Initial API Endpoints

POST /api/campaign

POST /api/lead

GET /api/analytics/{campaignID}

---

# Supabase Integration

Supabase must manage:

authentication  
database  
row-level security

---

# Performance Requirements

Landing pages must load under 2 seconds.

QR redirect must take under 300ms.

---

# Development Goal

The starter kit must produce a working MVP with:

campaign creation  
QR generation  
landing pages  
lead capture  
analytics dashboard