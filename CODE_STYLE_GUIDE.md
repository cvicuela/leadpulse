# LeadPulse Code Style Guide

This document defines the coding standards for the LeadPulse platform.

Claude must strictly follow these guidelines when generating or modifying code.

---

# General Principles

Code must always be:

- simple
- readable
- modular
- scalable
- mobile-first

Avoid unnecessary complexity.

Prefer clarity over clever code.

---

# File Organization

The project structure must remain clean and consistent.

Example:

/app  
/components  
/lib  
/api  
/qr  
/dashboard  
/database  

Each folder must contain files related only to its responsibility.

---

# Component Rules

Components must be:

- small
- reusable
- focused on a single responsibility

Example:

components/

LeadForm.tsx  
QRCard.tsx  
LandingHero.tsx  
CampaignStats.tsx

Never create large monolithic components.

---

# Function Rules

Functions must be:

- under 50 lines when possible
- descriptive
- pure when possible

Bad example:

handleAllCampaignLogic()

Good example:

createCampaign()  
generateQR()  
storeScanEvent()

---

# Naming Conventions

Variables:

camelCase

Functions:

camelCase

Components:

PascalCase

Example:

LeadForm.tsx  
CampaignCard.tsx

Database tables:

snake_case

Example:

campaigns  
qr_scans  
leads  

---

# API Naming

Endpoints must follow REST conventions.

Example:

POST /api/campaign  
GET /api/campaign/{id}  
POST /api/lead  

---

# Performance Rules

Landing pages must:

- load under 2 seconds
- avoid heavy dependencies
- minimize JavaScript bundles

Prefer server-side rendering when possible.

---

# Styling Rules

TailwindCSS must be used for all styling.

Avoid custom CSS unless necessary.

Design must be:

- minimal
- clean
- responsive

---

# Error Handling

All APIs must return structured responses.

Example:

{
  "status": "success"
}

or

{
  "status": "error",
  "message": "Invalid campaign ID"
}

---

# Security Rules

Never expose:

- API keys
- database credentials
- secrets

All secrets must be stored in environment variables.

---

# Final Principle

If unsure, Claude must prioritize:

simplicity > complexity