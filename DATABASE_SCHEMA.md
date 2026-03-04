# Database Schema

Supabase PostgreSQL

---

## campaigns

id  
tenant_id  
publisher_id  
advertiser_id  
industry  
location  
created_at

---

## scans

id  
campaign_id  
timestamp  
device  
geo  
referrer

---

## leads

id  
campaign_id  
name  
phone  
email  
created_at

---

## tenants

id  
organization_name  
type (publisher / advertiser / agency)