# Development Workflow

Claude must follow this workflow before coding.

1 Analyze repository structure  
2 Identify minimal modification  
3 Propose architecture change  
4 Generate patch code  
5 Verify compatibility  

---

## Code Rules

Components must be small and reusable.

Example:

/components
LeadForm.tsx
QRCard.tsx
LandingHero.tsx

---

## Utilities

Shared logic must go in:

/lib

Example:

/lib/qrGenerator.ts  
/lib/analytics.ts  
/lib/leadStorage.ts

---

## Performance

Landing page load time < 2 seconds

QR redirect time < 300ms