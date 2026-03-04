# LeadPulse MVP Build Prompt

You are the lead software architect and developer responsible for building the LeadPulse SaaS platform.

Before generating any code you must read and understand the following repository documents.

README.md  
SAAS_MODEL.md  
SYSTEM_ARCHITECTURE.md  
PRODUCT_ROADMAP.md  

CLAUDE.md  
CLAUDE_SYSTEM.md  

AI_DEVELOPMENT_MASTERPLAN.md  
AI_TASK_QUEUE.md  
AI_BUILDER_PROMPT.md  
BOOTSTRAP_PROMPT.md  

CODE_STYLE_GUIDE.md  
COMPONENT_LIBRARY.md  
DEVELOPMENT_WORKFLOW.md  
PROJECT_RULES.md  

DATABASE_SCHEMA.md  
PLATFORM_DATA_MODEL.md  
API_SPEC.md  

ENVIRONMENT_SETUP.md  
REPOSITORY_BLUEPRINT.md  
SAAS_STARTER_KIT.md  

You must understand the architecture before writing any code.

---

# Objective

Build the **LeadPulse MVP SaaS platform**.

The MVP must support:

QR campaigns  
AI landing pages  
lead capture  
analytics dashboard  

The system must be multi-tenant.

---

# Technology Stack

Frontend

Next.js  
React  
TailwindCSS  

Backend

Supabase  
PostgreSQL  

Deployment

Vercel

---

# Required Project Structure

/app  
/components  
/lib  
/api  
/qr  
/ai  
/dashboard  
/database  

Follow the repository blueprint when creating files.

---

# MVP Features

The platform must include the following features.

---

# Authentication

Implement authentication using Supabase Auth.

Users must be able to:

Sign up  
Login  
Access dashboard

Roles include:

publisher  
advertiser  
agency  

---

# Campaign Creation

Users must be able to create campaigns.

Campaign fields:

campaign_name  
industry  
location  
publisher_id  
advertiser_id  

Store campaigns in database.

---

# QR Code Engine

Each campaign must generate a dynamic QR code.

QR route:

/c/{campaignID}

QR scans must log:

timestamp  
device  
location  

Then redirect to landing page.

---

# Landing Pages

Create dynamic landing pages for each campaign.

Landing route:

/l/{campaignID}

Landing sections:

Hero  
Offer  
Lead Form  
WhatsApp Button  
Contact  

Landing pages must load in under 2 seconds.

---

# Lead Capture

Lead form fields:

name  
phone  
email  

Store leads in database.

Associate each lead with a campaign.

---

# Analytics Dashboard

Create dashboard showing campaign metrics.

Metrics include:

QR scans  
visits  
leads  
conversion rate  

Dashboard route:

/dashboard

---

# UI Components

Use components defined in:

COMPONENT_LIBRARY.md

Examples:

AppLayout  
CampaignCard  
QRGenerator  
LeadForm  
AnalyticsCard  

Do not duplicate components unnecessarily.

---

# Security

Implement:

input validation  
secure API routes  
environment variables  

Never expose secrets.

---

# Performance

QR redirect must be under 300ms.

Landing page load under 2 seconds.

Avoid heavy dependencies.

---

# Development Strategy

You must build the platform incrementally.

Step 1

Create project structure and Supabase connection.

Step 2

Implement authentication.

Step 3

Implement campaign creation.

Step 4

Implement QR code system.

Step 5

Implement landing pages.

Step 6

Implement lead capture.

Step 7

Implement analytics dashboard.

---

# Restrictions

Do NOT implement the following advanced systems yet.

Growth Engine  
Ad Performance Network  
Offline Attribution Engine  
Data Moat Architecture  

These systems are defined in future architecture documents and must be ignored during MVP development.

---

# Final Instructions

Before writing code:

Analyze the repository structure.

Then propose the minimal implementation plan.

Then begin building the LeadPulse MVP.