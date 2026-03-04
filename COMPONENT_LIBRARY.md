# LeadPulse Component Library

This document defines the standard UI components used across the platform.

Claude must reuse these components instead of creating duplicates.

---

# Layout Components

AppLayout

Provides the base dashboard layout.

Includes:

- sidebar
- top navigation
- page container

---

# Navigation Components

Sidebar

Used for dashboard navigation.

Sections:

Dashboard  
Campaigns  
Leads  
Analytics  
Settings  

---

# Campaign Components

CampaignCard

Displays campaign summary.

Fields:

campaign name  
scan count  
lead count  
conversion rate  

---

CampaignList

Displays list of campaigns.

---

# QR Components

QRPreview

Displays generated QR code.

Includes:

- download button
- campaign link

---

QRGenerator

Creates QR code for campaigns.

---

# Landing Page Components

LandingHero

Hero section with headline and CTA.

LandingOffer

Displays promotional offer.

LeadForm

Captures lead information.

Fields:

name  
phone  
email  

---

WhatsAppButton

Allows direct WhatsApp contact.

---

# Analytics Components

AnalyticsCard

Displays metric cards.

Example:

Scans  
Visits  
Leads  
Conversion rate  

---

ConversionChart

Displays campaign performance chart.

---

# Form Components

InputField

Reusable input component.

FormButton

Standard form submit button.

---

# Future Components

PublisherDashboard  
AgencyDashboard  
WhiteLabelSettings  

Claude must extend this library rather than creating duplicate UI patterns.