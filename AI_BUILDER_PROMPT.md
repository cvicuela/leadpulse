You are the lead software architect and engineer for the LeadPulse platform.

Before generating any code you must read and understand the following repository files:

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
BOOTSTRAP_PROMPT.md

Do not start coding until you understand the full architecture of the system.

---

# Project Summary

LeadPulse is a multi-tenant SaaS platform that converts offline advertising into measurable leads using QR campaigns and AI-generated landing pages.

Core flow:

QR Scan  
→ Landing Page  
→ Lead Capture  
→ Analytics Dashboard

The platform must support advertisers, publishers and agencies.

---

# Development Instructions

You must follow the implementation order defined in:

AI_TASK_QUEUE.md

Build the platform incrementally.

Never implement advanced features before the core platform works.

---

# Phase 1 Objective

Initialize the LeadPulse platform.

Create the base SaaS infrastructure.

Stack requirements:

Next.js  
React  
TailwindCSS  
Supabase  
PostgreSQL  

Hosting must be compatible with Vercel.

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

Follow the coding standards defined in:

CODE_STYLE_GUIDE.md

Reuse UI components defined in:

COMPONENT_LIBRARY.md

---

# Phase 1 Deliverables

Claude must implement:

1 Authentication system using Supabase Auth

2 Campaign creation interface

3 Database tables for:

tenants  
users  
campaigns  

4 Dashboard layout

5 Campaign list view

---

# Phase 2 Deliverables

QR Campaign Engine.

Generate dynamic QR codes.

Route format:

/c/{campaignID}

QR scans must record:

timestamp
device
location

---

# Phase 3 Deliverables

Landing page engine.

Route:

/l/{campaignID}

Landing pages must include:

Hero  
Offer  
Lead Form  
WhatsApp Button  
Contact  

Landing pages must load under 2 seconds.

---

# Phase 4 Deliverables

Lead capture system.

Store leads in database.

Associate leads with campaign.

---

# Phase 5 Deliverables

Analytics dashboard.

Display metrics:

QR scans  
visits  
leads  
conversion rate  

---

# Performance Constraints

Landing pages must load under 2 seconds.

QR redirect under 300ms.

Avoid heavy dependencies.

---

# Security Rules

Never expose secrets.

Use environment variables.

Implement input validation.

---

# Final Instructions

When generating code:

1 Analyze repository structure first
2 Create minimal files required
3 Ensure no broken imports
4 Ensure project builds successfully
5 Follow the architecture documents

Start by analyzing the repository and proposing the minimal implementation plan before writing code.