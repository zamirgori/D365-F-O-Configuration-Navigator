# D365 Configuration Navigator

> A structured, searchable reference tool for configuring a new Microsoft Dynamics 365 Finance & Operations legal entity — built as a single-file web application with a Clinical SaaS Blueprint design system.

---

## Overview

The **D365 Configuration Navigator** transforms a dense, 44-item ERP configuration checklist into an intuitive, data-dense web application. Designed for ERP consultants, solution architects, and implementation teams who need fast, reliable access to configuration guidance without wading through multi-page spreadsheets.

Built as a single self-contained HTML file — no server, no dependencies, no build step. Open it in any browser and it works.

---

## Screenshot

```
┌──────────────────────────────────────────────────────────────────┐
│  🔷 D365 Navigator   Home › Dashboard          [Search] [Modules]│
├────────────┬─────────────────────────────────────────────────────┤
│  Overview  │  D365 F&O Configuration Navigator                   │
│  Dashboard │  v1.0 · Supply Chain Org · April 2025               │
│  All Mods  │                                                      │
│            │  ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐              │
│  Chapters  │  │  7   │ │  13  │ │  11  │ │  13  │              │
│  ○ Org (7) │  │Org   │ │Fin   │ │SCM   │ │ Inv  │              │
│  ○ Fin(13) │  └──────┘ └──────┘ └──────┘ └──────┘              │
│  ○ SCM(11) │                                                      │
│  ○ Inv(13) │  Chapter I ░░░░░░░░░░░░░░ 86%   7 tasks            │
│            │  Chapter II ████████████ 100%  13 tasks            │
│  Tools     │  Chapter III ░░░░░░░░░░░ 73%   11 tasks            │
│  Search    │  Chapter IV ░░░░░░░░░░░  69%   13 tasks            │
│  About     │                                                      │
└────────────┴─────────────────────────────────────────────────────┘
```

---

## Features

### Navigation
- **Fixed topbar** with live breadcrumb trail that updates as you navigate
- **Fixed sidebar** with module chapters, per-chapter task counts, and collapsible sub-navigation
- **Chapter TOC panel** for fast in-page jumping within any module
- **Mobile-responsive** with sidebar toggle for smaller screens

### Dashboard
- Per-module KPI stat cards showing total tasks and mandatory/optional split
- Visual progress strip with completion percentage bars per chapter
- Implementation sequence notice (Org Admin → Finance → SCM → Inventory)

### Module Chapters
- Table-style configuration rows: task number, name, module badge, mandatory/optional status
- **Expandable detail panels** with three columns:
  - Task description
  - Business questions → sample answers
  - D365 F&O navigation path (monospace)
- Highlighted border on expanded cards for visual focus
- Per-chapter KPI summary (total, mandatory, optional counts)

### Search & Filter
- Full-width search across all fields: task name, description, D365 config path, Q&A content
- Module filter chips: All · Org Admin · Finance · SCM · Inventory
- Status filter chips: All · Mandatory · Optional
- Results show module badge, chapter reference, and one-click jump-to-card
- Quick search in topbar triggers search screen instantly

### About
- Project overview, content source, and design system documentation
- Numbered implementation sequence notes
- MIT License text

---

## Content

All configuration content is derived from the **Microsoft Dynamics 365 F&O New Legal Entity Configuration Checklist** (Supply Chain Organization, Version 1.0, April 2025).

### Modules & Task Count

| Chapter | Module | Tasks | Mandatory | Optional |
|---------|--------|-------|-----------|----------|
| I | Org Administration | 7 | 6 | 1 |
| II | Finance | 13 | 13 | 0 |
| III | Supply Chain (SCM) | 11 | 8 | 3 |
| IV | Inventory Management | 13 | 9 | 4 |
| **Total** | | **44** | **36** | **8** |

### Configuration Areas Covered

**Org Administration**
- Legal Entity creation
- Operating Units & Hierarchy
- Number Sequences
- Currencies & Exchange Rate Types
- Units of Measure
- Global Address Book (GAB) Parameters
- Working Time Calendars

**Finance**
- Ledger Setup
- Fiscal Calendar & Periods
- Chart of Accounts
- Financial Dimensions
- Account Structures & Rules
- Bank Accounts
- Payment Terms
- Payment Methods (AP & AR)
- Sales Tax Setup
- Vendor Groups & Posting Profiles
- Customer Groups & Posting Profiles
- Journal Names

**Supply Chain Management**
- Procurement Parameters
- Procurement Categories
- Vendor Setup
- Purchase Agreements
- Request for Quotation (RFQ)
- Charges (AP)
- Sales Parameters
- Customer Setup
- Charges (AR)
- Delivery Terms & Modes
- Trade Agreements & Pricing

**Inventory Management**
- Inventory Parameters
- Sites & Warehouses
- Locations & Zones
- Storage Dimension Groups
- Tracking Dimension Groups
- Item Model Groups
- Item Groups
- Product Masters & Released Products
- Inventory Costing & Closing
- Inventory Journals
- Cycle Counting
- Quality Management
- ABC Classification

---

## Getting Started

### Usage

1. **Download** `d365_saas_blueprint.html`
2. **Open** the file in any modern browser (Chrome, Firefox, Edge, Safari)
3. **Navigate** using the sidebar, topbar, or module cards
4. **Search** using the topbar quick-search or the dedicated Search & Filter screen

No installation, no server, no internet connection required after the initial load. Google Fonts (Geist) are loaded from the web — the app functions fully offline but will fall back to system fonts if fonts are unavailable.

### Sharing

Because the entire application is a single HTML file, sharing is as simple as:
- Emailing the `.html` file directly
- Uploading to a shared drive (SharePoint, OneDrive, Google Drive)
- Hosting on any static file server or CDN

---

## Design System

**Theme:** Clinical SaaS Blueprint

Inspired by modern enterprise SaaS applications (Linear, Notion, Vercel). Optimized for consultant workflows — data-dense, fast to scan, and familiar to power users.

| Token | Value |
|-------|-------|
| Primary background | `#F0F4F8` |
| Surface | `#FFFFFF` |
| Accent / Primary | `#0057FF` (Electric Blue) |
| Success | `#00875A` |
| Warning | `#B45309` |
| Border | `#D6DCE8` |
| Body text | `#0D1117` |
| Muted text | `#6B7591` |
| Heading font | Geist (700 weight) |
| Body font | Geist (400/500 weight) |
| Monospace font | Geist Mono |
| Border radius | 6px (elements) · 8px (cards) · 12px (panels) |

### Module Color Coding

| Module | Color | Hex |
|--------|-------|-----|
| Org Administration | Electric Blue | `#0057FF` |
| Finance | Forest Green | `#00875A` |
| Supply Chain | Amber | `#B45309` |
| Inventory | Berry | `#9C2B6B` |

---

## Sample Data

All business questions and answers reference a representative company profile:

- **Company:** Contoso Supply Co.
- **Country:** United States (USA)
- **Accounting currency:** USD
- **Additional currencies:** EUR, CAD, MXN
- **Sites:** US-01 (Main Plant, Seattle) · US-02 (Distribution, Dallas)
- **Departments:** Procurement, Sales, Warehouse
- **Costing methods:** Standard Cost (Finished Goods) · FIFO (Raw Materials) · Weighted Average (Packaging)

> ⚠️ All sample answers are illustrative defaults. Review and confirm with client business stakeholders during Fit-Gap Analysis workshops before any configuration is applied.

---

## Implementation Notes

1. **Follow the configuration sequence.** Org Administration must be complete before Finance; Finance before SCM; SCM before Inventory. Dependencies flow in this order.

2. **Validate all sample answers** with client business stakeholders during Fit-Gap Analysis workshops. Nothing in this tool should be treated as a confirmed client decision.

3. **Number sequences** must be reviewed against local regulatory requirements before finalizing — consecutive invoice numbering is required by many tax authorities.

4. **Costing methods** (Standard Cost, FIFO, Weighted Average) are legally binding once inventory transactions exist. Confirm with the client's Finance and Accounting team before configuration.

5. **Advanced Warehouse Management (WMS)** licensing must be confirmed with Microsoft licensing before enabling location-level or license plate tracking.

6. **Security roles and data access** should be configured in parallel with functional setup. This tool covers functional configuration only — refer to a separate Security Configuration workbook.

7. **Data migration** (Chart of Accounts, Item master, Vendor/Customer master, Opening Balances) should be tracked on a separate Data Migration Tracker.

---

## File Structure

```
d365_saas_blueprint.html    ← Entire application (single file)
README.md                   ← This file
```

The application is entirely self-contained within the single HTML file:

```
d365_saas_blueprint.html
├── <style>          CSS design system, layout, components
├── HTML             Topbar, sidebar, screen shells
└── <script>         Data (MODULES[], DATA[]), routing, rendering, search
```

---

## Browser Support

| Browser | Support |
|---------|---------|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Safari 14+ | ✅ Full |
| IE 11 | ❌ Not supported |

---

## License

MIT License

Copyright © 2025 D365 Configuration Navigator Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

---

## Acknowledgements

- **Content source:** Microsoft Dynamics 365 F&O New Legal Entity Configuration Checklist, Supply Chain Organization (Version 1.0, April 2025)
- **Typography:** [Geist](https://vercel.com/font) by Vercel
- **Design inspiration:** Linear, Notion, Vercel dashboard aesthetics
