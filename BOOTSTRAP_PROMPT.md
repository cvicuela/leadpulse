# LeadPulse Bootstrap Prompt

This document instructs Claude Code how to initialize and bootstrap the LeadPulse SaaS platform.

Claude must read the following files before generating any code:

README.md  
CLAUDE.md  
CLAUDE_SYSTEM.md  
SYSTEM_ARCHITECTURE.md  
PRODUCT_ROADMAP.md  
DATABASE_SCHEMA.md  
DEVELOPMENT_WORKFLOW.md  
AI_PROMPTS.md  
SAAS_MODEL.md  
API_SPEC.md  
AI_DEVELOPMENT_MASTERPLAN.md  
CODE_STYLE_GUIDE.md  
COMPONENT_LIBRARY.md  
AI_TASK_QUEUE.md  

Claude must fully understand the project architecture before starting development.

---

# Objective

Initialize the LeadPulse platform following the architecture defined in the repository documentation.

The platform must support:

QR campaigns  
AI landing pages  
lead capture  
analytics dashboards  
publisher SaaS accounts  

---

# Step 1 — Initialize Project

Claude must create a Next.js project using modern best practices.

Requirements:

Next.js (latest stable)  
React  
TailwindCSS  

Create base structure:

/app  
/components  
/lib  
/api  
/qr  
/ai  
/dashboard  
/database  

---

# Step 2 — Setup Supabase

Claude must configure Supabase integration.

Create connection utilities inside:

/lib/supabase.ts

Environment variables required:

SUPABASE_URL  
SUPABASE_ANON_KEY  

---

# Step 3 — Authentication

Create authentication system using Supabase Auth.

Users must be able to:

Sign up  
Login  
Access dashboard  

Roles:

publisher  
advertiser  
agency  

---

# Step 4 — Campaign Engine

Create campaign creation interface.

Campaign fields:

campaign_name  
industry  
publisher_id  
advertiser_id  
location  

Generate unique campaign ID.

Store in database.

---

# Step 5 — QR Code System

Claude must implement QR generation.

Campaign QR URL format:

/c/{campaignID}

QR scans must log:

timestamp  
device  
location  

Redirect to landing page.

---

# Step 6 — Landing Page Engine

Create dynamic landing pages.

Landing route:

/l/{campaignID}

Landing sections:

Hero  
Offer  
Lead Form  
WhatsApp CTA  
Contact  

Landing pages must load under 2 seconds.

---

# Step 7 — Lead Capture

Create lead form component.

Fields:

name  
phone  
email  

Store leads in Supabase.

Associate with campaign ID.

---

# Step 8 — Analytics Dashboard

Create dashboard showing:

QR scans  
visits  
leads  
conversion rate  

Dashboard route:

/dashboard

---

# Step 9 — UI Components

Claude must reuse components defined in:

COMPONENT_LIBRARY.md

Avoid duplicating components.

---

# Step 10 — Performance

Ensure:

Landing pages load under 2 seconds.

QR redirects under 300ms.

Avoid heavy dependencies.

---

# Step 11 — Security

Claude must implement:

input validation  
rate limiting  
secure APIs  
environment variables  

Never expose secrets.

---

# Step 12 — Output

Claude must:

Create all required project files  
Organize folders correctly  
Ensure project builds successfully  
Ensure no broken imports  

---

# Final Rule

Claude must always:

1. analyze repository
2. make minimal modifications
3. reuse components
4. maintain clean architecture