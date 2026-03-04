# LeadPulse System Architecture

LeadPulse is a **multi-tenant SaaS platform**.

Actors:

Publisher  
Advertiser  
Agency  

Example:

Magazine sells ad  
→ advertiser gets QR code  
→ user scans  
→ landing page  
→ lead captured  
→ analytics dashboard

---

## Multi-Tenant Model

Each organization has isolated data.

Key identifiers:

tenant_id  
organization_id  
campaign_id

---

## Campaign Engine

Each campaign contains:

campaign_id  
publisher_id  
advertiser_id  
industry  
location  
created_at

Campaign types:

magazine_ad  
billboard  
event  
real_estate  
retail

---

## QR Code Engine

Each campaign generates dynamic QR:

leadpulse.com/c/{campaignID}

All scans must record:

timestamp  
device  
geo  
referrer