# LeadPulse AI Development Task Queue

This file defines the order in which Claude should implement features.

Claude must complete tasks sequentially.

Do not skip phases.

---

# Phase 1 — Core Infrastructure

Tasks:

- Initialize Next.js project
- Configure TailwindCSS
- Connect Supabase
- Create authentication system

Pages:

/login  
/dashboard  

---

# Phase 2 — Campaign Engine

Tasks:

Create campaign creation UI.

Create database table:

campaigns

Generate campaign IDs.

---

# Phase 3 — QR Code System

Tasks:

Generate QR codes.

Create route:

/c/{campaignID}

Log QR scans.

Store scan metadata.

---

# Phase 4 — Landing Pages

Tasks:

Create AI landing page generator.

Landing must include:

Hero  
Offer  
Lead Form  
WhatsApp CTA  

---

# Phase 5 — Lead Capture

Tasks:

Create leads table.

Capture form submissions.

Store leads.

Allow lead export.

---

# Phase 6 — Analytics Dashboard

Tasks:

Create campaign metrics.

Display:

QR scans  
visits  
leads  
conversion rate  

---

# Phase 7 — Publisher Dashboard

Tasks:

Allow publishers to manage campaigns.

Create advertiser assignments.

---

# Phase 8 — White Label

Tasks:

Custom domains.

Custom branding.

Publisher analytics.

---

# Phase 9 — Optimization

Tasks:

AI landing optimization.

Conversion improvements.

Campaign comparison.

---

# Rule

Claude must:

- finish current phase
- validate functionality
- then move to the next phase