# LeadPulse API Specification

This document defines the internal API architecture.

---

# Base URL

/api/

---

# Campaign API

Create Campaign

POST /api/campaign

Request:

{
  "tenant_id": "string",
  "publisher_id": "string",
  "advertiser_id": "string",
  "industry": "string",
  "location": "string"
}

Response:

{
  "campaign_id": "uuid",
  "qr_url": "leadpulse.com/c/123"
}

---

# QR Scan Endpoint

GET /c/{campaignID}

Function:

- record scan
- detect device
- detect geo
- redirect to landing page

---

# Lead Submission

POST /api/lead

Request:

{
  "campaign_id": "string",
  "name": "string",
  "phone": "string",
  "email": "string"
}

Response:

{
  "status": "success"
}

---

# Analytics Endpoint

GET /api/analytics/{campaignID}

Response:

{
  "scans": 120,
  "visits": 98,
  "leads": 32,
  "conversion_rate": "32%"
}

---

# Authentication

Future versions will support:

JWT authentication
API keys
OAuth integrations

---

# Future Integrations

HubSpot
Salesforce
Google Ads
Meta Ads
WhatsApp CRM