# LeadPulse Environment Setup

This document defines the required environment variables and setup.

---

# Required Services

LeadPulse depends on the following services:

Supabase  
Vercel  
GitHub  

Optional:

Cloudflare CDN

---

# Environment Variables

The following variables must exist:

SUPABASE_URL
SUPABASE_ANON_KEY

NEXT_PUBLIC_BASE_URL

---

# Development Setup

Install dependencies:

npm install

Run development server:

npm run dev

---

# Production Deployment

The platform must be deployed using Vercel.

Environment variables must be configured inside the Vercel dashboard.

---

# Security

Environment variables must never be committed to GitHub.

Use:

.env.local