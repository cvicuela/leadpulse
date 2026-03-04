# LeadPulse Offline Attribution Engine

This document defines the Offline Attribution Engine of LeadPulse.

This system enables LeadPulse to track the performance of physical advertising placements.

The Offline Attribution Engine must not be implemented during the initial MVP build.

It is part of the advanced analytics layer of the platform.

---

# Vision

LeadPulse becomes the analytics layer for offline advertising.

Example attribution chain:

Ad Placement
→ QR Scan
→ Landing Page
→ Lead Capture
→ Conversion

The system measures how physical ads generate digital results.

---

# Attribution Data Sources

The attribution engine combines several signals:

QR scan data  
campaign metadata  
location data  
time of scan  
device information  

This allows the system to determine which advertising placements generate results.

---

# Attribution Objects

The engine tracks several objects.

Publisher  
Ad Placement  
Campaign  
Scan  
Lead  
Conversion  

Each object contributes to attribution calculations.

---

# Ad Placement Tracking

Each campaign must be associated with a placement.

Examples:

Magazine issue  
Billboard location  
Event booth  
Real estate sign  
Restaurant table display  

Placement fields:

placement_id  
publisher_id  
location  
placement_type  
placement_description

---

# Attribution Model

LeadPulse will support several attribution models.

First Scan Attribution

The first QR scan receives full credit.

Last Interaction Attribution

The last interaction before lead submission receives credit.

Weighted Attribution

Multiple scans share attribution weight.

---

# Attribution Metrics

The system calculates several key metrics.

Scan Rate

number of scans per placement

Lead Conversion Rate

percentage of scans that generate leads

Placement Efficiency

leads generated per campaign placement

---

# Placement Performance Ranking

Placements will be ranked based on:

scan volume  
lead conversion rate  
lead quality score  

This allows advertisers to compare different physical advertising channels.

---

# Analytics Output

Example placement report:

Publisher: Real Estate Magazine  
Placement: April Issue Full Page

Scans: 1,240  
Leads: 142  
Conversion Rate: 11.4%

---

# Integration With Campaigns

Campaigns must include:

placement_id

This allows attribution reports to connect scans and leads with the physical ad placement.

---

# Future AI Attribution

Future AI systems may analyze attribution data to:

predict campaign performance  
recommend better placements  
optimize advertising budgets

---

# Implementation Rule

Claude must not implement the Offline Attribution Engine during MVP development.

The system must first support:

QR campaigns  
landing pages  
lead capture  
analytics dashboards

Only after these modules are stable can attribution features be added.