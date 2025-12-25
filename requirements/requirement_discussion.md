# Vihara Medical / SafeSphere — Requirements & Phase-wise Roadmap

## 1. Business Context & Current Situation

Vihara Medical originally began with home COVID testing and has evolved into a multi-service healthcare provider. Current services include:

- Physiotherapy at home (primary revenue driver)
- SafeSphere mental health services
- Nursing (home visits)
- Lab investigations (part in-house, largely outsourced)
- Pharmacy
- In-center physiotherapy
- Clinic with visiting doctors

**Current operational model**
- Leads come mostly via Google Ads
- Central call/ops team manages all services
- Mix of full-time and freelancer therapists
- Scheduling and tracking are highly manual (Excel + WhatsApp)
- Business is currently loss-making but growing
- Biggest constraint is **operational scalability**, not demand

---

## 2. Strategic Priorities

### 2.1 Highest priorities
1. Physiotherapy at home  
2. SafeSphere mental health services  

### 2.2 Maintain-but-don’t-scale aggressively
- Lab investigations
- Pharmacy standalone walk-in retail
- General “home services bundle”
- In-center clinics purely for walk-in OPD

---

## 3. High-Level Goals

### 3.1 Business goals
- 4× physiotherapy sessions per month
- Improve conversion from:
  - enquiry → first visit → package
- Reduce dependence on key ops individuals
- Enable multi-city scalability
- Build consolidated mental health platform
- Improve unit economics and profitability

### 3.2 Technology goals
- Replace spreadsheets with structured system
- Build mobile-first operations platform
- Automate:
  - lead management
  - assignment
  - routing
  - follow-ups
- Avoid leakage to freelancers
- Support subscription pharmacy delivery
- Data-driven dashboards

---

## 4. Stakeholders & User Types

- Call center / operations executives
- Operations manager / head of operations
- Physiotherapists (employees)
- Physiotherapists (freelancers)
- Psychologists & mental health therapists
- Supervisors / field coordinators
- Patients / customers
- Finance & accounting
- Marketing team
- Management / founders

---

## 5. Core Business Modules Required

### 5.1 Lead & Enquiry Management
- Capture enquiries from:
  - Google Ads
  - phone calls
  - WhatsApp
  - website
  - referrals
- Multiple service types
- Structured intake questionnaire
- Language preference (ex: Telugu)
- Priority scoring
- Follow-up tracking
- Lead status pipeline

---

### 5.2 Operations & Scheduling

- Therapist & supervisor calendars
- Zone mapping of city
- First visit vs repeat visit identification
- Package session tracking
- Online vs in-person session handling
- Automated reminder system
- Safety workflows for home visits

---

### 5.3 Resource Management

#### Physiotherapists & Mental Health Professionals

- employee / freelancer flag
- specialties and tags
- location / serviceable zones
- availability
- conversion rate metrics
- document storage (licenses, ID etc.)

---

### 5.4 Mental Health Module (SafeSphere)

- Therapy plan lifecycle
- Confidential clinical notes
- Strict role-based privacy controls
- Therapist-patient matching
- Support for de-addiction & family therapy
- Online + in-person session handling

> Management should not have access to patient issue-level data.

---

### 5.5 Physiotherapy Module

- Initial assessment visit
- Package definition
- Conversion tracking:
  - enquiry
  - first session
  - package
- Supervisor attendance
- Outcome tracking

---

### 5.6 Finance & Billing

- Package billing engine
- Split revenue with freelancers
- Freelancer payout calculation
- Online payment integration
- Refund workflows
- Profitability per:
  - therapist
  - service
  - zone
  - campaign

---

### 5.7 Marketing & Analytics

- Lead-source tracking
- Age/geography segmentation
- Google Ads integration
- Conversion funnel tracking
- Demand heatmaps by zone
- CAC vs revenue

---

### 5.8 Pharmacy Module (Later Phase)

- Inventory & stock
- Prescription upload
- Monthly subscription plans
- Automated delivery routing
- Order labeling/packaging workflows

---

## 6. Data & Dashboard Requirements

### 6.1 Key Metrics Needed

- Total enquiries by service
- Enquiry → first-session conversion
- First-session → package conversion
- Active therapists by zone
- Supervisor utilization
- City heatmap of demand
- Revenue vs marketing cost
- Leakage detection
- Monthly revenue per module
- Employee vs freelancer contribution

### 6.2 Required Dashboards

- CEO dashboard
- Operations live map
- Zone heatmap
- Marketing dashboard
- Therapist leaderboard
- Profitability dashboard

---

## 7. Current Pain Points

- Excel-based manual workflow
- WhatsApp as operational system
- Heavy dependence on 1–2 key people
- No routing map
- Limited supervisor visibility
- High cognitive load on operations staff
- Poor follow-up visibility
- Leakage to freelancers
- Marketing cannot scale due to ops bandwidth limits

---

# 8. Phase-wise Implementation Roadmap

## Phase 0 — Discovery & System Design

**Focus**
- Interview teams
- Map all workflows
- Define database models
- Choose approach:
  - ERPNext module customization
  - Custom Frappe app
- Role & permission mapping
- Data migration plan from Excel

---

## Phase 1 — Lead & Operations Backbone (Start Here)

Deliverables:

- Central enquiry capture
- Call center console
- Lead statuses and pipelines
- Basic therapist matching
- Session scheduling
- Ops notes & call log entries

**Outcome**
- Single source of truth
- Remove dependence on spreadsheets

---

## Phase 2 — Mobile-first Field Operations

Deliverables:

- Mobile UI for ops team
- Supervisor assignment system
- Geo-zones
- Live map view (“who is where now”)
- Check-in / check-out validation
- Female therapist safety workflows

**Outcome**
- Real-time field visibility
- Reduced manual routing

---

## Phase 3 — Finance, Billing & Leakage Control

Deliverables:

- Invoicing
- Online payment links
- Package billing engine
- Freelancer payout automation
- Suspicious pattern detection
- Revenue & cost dashboards

**Outcome**
- Improved unit economics visibility

---

## Phase 4 — SafeSphere Mental Health Platform

Deliverables:

- Therapist discovery
- Secure note-taking
- Role-based confidentiality
- Online session scheduling
- De-addiction & couple/family therapy flows

**Outcome**
- Dedicated scalable mental health product

---

## Phase 5 — Automation & Intelligence Layer

Deliverables:

- Auto routing
- Lead scoring
- Follow-up automation (WhatsApp/SMS)
- Renewal reminders
- Satisfaction feedback flows
- Demand prediction per zone

---

## Phase 6 — Pharmacy Subscription & Delivery

Deliverables:

- Subscription refills
- Recurring billing
- Delivery routing
- Inventory sync with ERPNext
- Combination care plans

---

## 9. Risks & Mitigations

| Risk | Mitigation |
|------|-----------|
| Ops overwhelmed | phased rollout |
| Data migration errors | run systems in parallel |
| Leakage to freelancers | contract + in-app scheduling |
| Privacy issues (mental health) | strict RBAC & encryption |
| Supervisor overload | auto-routing |

---

## 10. Recommended Next Steps

1. Freeze Phase-0 discovery workshop
2. Gather:
   - existing Excel files
   - Google Forms
   - present weekly/daily reports
3. Decide technical direction:
   - ERPNext-only
   - hybrid
   - custom Frappe app
4. Start with **Physiotherapy module first**
5. Define exact dashboards required by management

---

## 11. Notes on Tech Approach

- Likely best architecture:
  - ERPNext for finance, stock, pharmacy
  - Custom Frappe app for ops and dispatch engine
- Must be **mobile-first**
- Must support multi-city growth

