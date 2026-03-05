# TurboFSM — Field Service Management Wireframes

High-fidelity HTML/CSS wireframes for the TurboFSM platform, covering the **Customer Portal** and **Superadmin** interfaces.

## Tech Stack

- Pure HTML5 / CSS3 / Vanilla JavaScript (no frameworks)
- Google Fonts (DM Sans)
- Single shared stylesheet: `style.css`
- Client-side filtering and search (no backend)

## Project Structure

```
wireframes/
├── turbofsm-portal/          # Main customer-facing portal (40 HTML + 1 CSS)
│   ├── style.css             # Shared design system (CSS custom properties)
│   ├── dashboard.html        # Main entry point after login
│   ├── landing.html          # Public marketing page
│   ├── signin.html           # Authentication
│   ├── registration.html     # New user signup
│   └── ...                   # Feature pages (see modules below)
└── README.md
```

## Portal Modules

### Sales & CRM (13 pages)
Lead management, appointments, scheduling, estimates, and customer database.

| Page | Description |
|------|-------------|
| `lead-manager.html` | Lead pipeline with source tracking and status filters |
| `lead-form.html` | Create/edit lead form |
| `appointments.html` | Appointment list view |
| `create-appointment.html` | New appointment creation |
| `appointment-details.html` | Appointment detail view |
| `estimates.html` | Estimate list and management |
| `create-estimate.html` | Build new estimate with line items |
| `estimate-template.html` | Custom estimate template upload |
| `customers.html` | CRM customer database with lifetime value tracking |
| `customer-edit.html` | Customer profile editor |
| `customer-estimates.html` | Customer's estimate history |
| `customer-jobs.html` | Customer's job history |
| `customer-invoices.html` | Customer's invoice history |

### Operations (8 pages)
Job management, floor planning, scheduling, and crew cost tracking.

| Page | Description |
|------|-------------|
| `jobs-board.html` | Kanban-style job board |
| `create-job.html` | New job creation form |
| `job-detail.html` | Job detail with multi-tab interface |
| `job-cost-sheet.html` | Job financials and cost tracking |
| `job-invoice.html` | Invoice linked to a job |
| `floor-plan.html` | Interactive floor plan designer |
| `schedule.html` | Calendar/schedule view |
| `crew-costs.html` | Labor cost tracking |

### Invoicing & Billing (5 pages)
Invoice creation, tracking, and payment recording.

| Page | Description |
|------|-------------|
| `invoicing.html` | Invoice list with payment status |
| `create-invoice.html` | Create new invoice |
| `invoice-details.html` | Invoice detail with line items |
| `invoice-template.html` | Custom invoice template upload |
| `record-payment.html` | Record payment against an invoice |

### Setup & Configuration (9 pages)
Business settings, catalogs, and team management.

| Page | Description |
|------|-------------|
| `management-master.html` | Configuration hub |
| `nomenclature.html` | Industry terminology settings |
| `materials.html` | Material catalog |
| `services.html` | Service catalog |
| `crew-management.html` | Team/employee management |
| `currency-settings.html` | Currency configuration |
| `sites-management.html` | Service location management |
| `artifact-library.html` | Floor plan symbol library |
| `client-settings.html` | Business profile settings |

### Auth & Marketing (4 pages)
`landing.html`, `signin.html`, `registration.html`, `pricing.html`

### Showcase (1 page)
`profile-presentation.html` — Public business profile page.

## Design System

- **CSS Custom Properties**: 22 design tokens for colors, spacing, shadows, and transitions
- **Color Palette**: Accent blue (`#0f6fde`), teal, orange, red, green, purple + light variants
- **Status Pills**: 20+ semantic states (e.g., `st-paid`, `st-draft`, `st-active`, `st-overdue`)
- **Layout**: Fixed 244px dark sidebar + sticky topbar + flexible content area
- **Components**: KPI cards, data tables, filter chips, forms (2-col grid), modals, collapsible sections, crew avatars

## Navigation Structure

Sidebar groups:
1. **Main** — Dashboard
2. **Sales** — Lead Manager, Appointments, Schedule, Estimation, Customers
3. **Operations** — Floor Plan, Jobs Board, Invoicing, Crew Costs
4. **Showcase** — Profile & Presentation
5. **Setup** — Management Master, Client Settings

## User Flow

```
Landing → Sign In → Dashboard
  ├── Sales: Leads → Appointments → Estimates → Customers
  ├── Operations: Jobs Board → Job Detail → Crew & Costs
  ├── Invoicing: Create Invoice → Track → Record Payment
  └── Setup: Business Config, Materials, Services, Crew
```
