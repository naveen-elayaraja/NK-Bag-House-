# NK Bag House — Website Architecture Plan

## 1. Project Goal

Build a responsive business website for **NK Bag House**, a bulk bag manufacturer. The website should help prospective customers discover products, understand available options, and send clear enquiries for standard or custom bulk requirements.

The initial order range communicated for the business is **10 to 100,000 pieces**. Product specifications, exact catalogue items, pricing rules, and enquiry-handling procedures must be confirmed with the business before they are implemented.

## 2. Product Scope

### MVP — Customer-facing website

1. **Home** — business introduction, key value proposition, product categories, and a clear enquiry call to action.
2. **Products** — browsable product catalogue with images and concise specifications.
3. **Product details** — product-specific information and an enquiry action.
4. **Custom / Bulk Enquiry** — form for contact details, product or requirement, quantity, and optional message or reference attachment.
5. **About** — business background, capabilities, and relevant manufacturing information.
6. **Contact** — verified phone, email, address, and other approved contact channels.

### Later, only if the business needs them

- Admin interface to manage products and review enquiries.
- Customer accounts and enquiry history.
- Inventory, order tracking, quotations, online payments, or CRM integration.

These are not part of the initial build unless requirements confirm their value.

## 3. High-Level Architecture

The proposed separation is:

```text
Customer
   |
   v
Web Browser (Desktop / Mobile)
   |
   v
Next.js Website
   |                     |
   | Public pages        | Enquiry submission
   v                     v
Product content       Backend API (to be selected)
                            |
                 +----------+----------+
                 |                     |
                 v                     v
             Database             File Storage
           (if required)          (optional)
```

The browser should never connect directly to a database or expose private credentials. Any operation that stores enquiries, handles uploads, or performs privileged actions must go through a server-side API.

## 4. Technology Direction

| Layer | Current direction | Decision status |
|---|---|---|
| Frontend | Next.js 16, React, TypeScript, Tailwind CSS | Selected |
| Routing | Next.js App Router | Selected with frontend setup |
| Backend API | Python + FastAPI is the current candidate | Not finalized |
| Database | PostgreSQL is the current candidate | Not finalized |
| Product images / uploads | Managed object or image storage, if needed | Not finalized |
| Hosting | Frontend and API hosting to be chosen after deployment requirements are known | Not finalized |

The frontend foundation is being developed first. Backend, database, storage, and hosting choices should be revisited after the UI reference, enquiry workflow, expected traffic, maintenance needs, and budget are understood.

## 5. Main Data Concepts

The following are conceptual entities, not a finalized database schema.

### Product

- Product identifier
- Name and category
- Short and detailed description
- Images
- Specifications and available options
- Publication status

### Enquiry

- Enquiry identifier
- Customer name
- Business name (optional)
- Email and phone
- Product or requirement description
- Requested quantity
- Additional message
- Optional reference-file metadata
- Submission time and enquiry status

Do not store unnecessary personal information. Validate all submitted fields on the server. Define retention and access rules before collecting customer data.

## 6. Key User Flows

### Browse products

1. Visitor opens the home page.
2. Visitor explores product categories or the catalogue.
3. Visitor opens a product detail page.
4. Visitor chooses to enquire about that product.
5. The enquiry form carries the selected product context.

### Submit a custom or bulk enquiry

1. Visitor opens the enquiry page.
2. Visitor provides contact information and requirement details.
3. The website validates required fields.
4. The server validates the submission again and stores it.
5. The visitor receives a clear success or error response.
6. The business receives or can access the enquiry through an agreed notification or admin workflow.

The notification method and enquiry ownership process must be agreed before implementation. A successful form response must not be shown unless the server confirms that the enquiry was accepted.

## 7. Frontend Structure (Planned)

A maintainable starting structure:

```text
frontend/
├── app/
│   ├── page.tsx                 # Home
│   ├── products/
│   │   ├── page.tsx             # Product catalogue
│   │   └── [slug]/page.tsx      # Product details
│   ├── enquiry/page.tsx         # Bulk/custom enquiry
│   ├── about/page.tsx
│   └── contact/page.tsx
├── components/
│   ├── layout/                  # Header, footer, navigation
│   ├── products/                # Product cards and catalogue UI
│   └── forms/                   # Reusable form controls
├── lib/                         # Shared utilities and API client
├── public/                      # Static assets
└── types/                       # Shared TypeScript types
```

This is a target structure, not a requirement to create every route or folder immediately. Components should be introduced when they are needed.

## 8. Quality, Security, and Accessibility

- Mobile-first responsive layouts and clear navigation.
- Semantic HTML, keyboard support, visible focus states, and accessible form labels.
- Optimized product images and sensible page-loading performance.
- Server-side validation for all submitted data.
- Secrets stored in environment variables and excluded from Git.
- Rate limiting and spam protection on public enquiry endpoints before production.
- Restrict administrative access if an admin interface is introduced.
- Use HTTPS in production and collect only information needed to respond to enquiries.
- Provide clear loading, validation, success, and failure states.
- Test core pages and enquiry submission on mobile and desktop before launch.

## 9. Delivery Phases

| Phase | Work | Exit condition |
|---|---|---|
| 0. Requirements | Confirm products, specifications, contact details, enquiry fields, and reference UI | Approved scope and content |
| 1. UI foundation | Establish design tokens, layout, navigation, and responsive page shell | UI direction approved |
| 2. Public pages | Build home, catalogue, product details, about, and contact pages | Pages reviewed on mobile and desktop |
| 3. Enquiry workflow | Implement form, server validation, persistence, and agreed notification | End-to-end enquiry tested |
| 4. Content management | Add admin/product management only if required | Business can maintain required content |
| 5. Production launch | Configure hosting, domain, environment variables, monitoring, backups, and security checks | Production smoke test passes |

## 10. Open Decisions

The following must be confirmed before the related implementation begins:

- Final UI reference, brand colours, typography, and logo assets.
- Actual product categories, images, dimensions, materials, and other specifications.
- Whether prices should be displayed or all sales should be enquiry-based.
- Required enquiry fields and allowed attachment types / size limits.
- Who receives enquiries and how quickly they are expected to respond.
- Whether the business needs an admin dashboard.
- Backend, database, storage, and hosting choices.
- Domain name, budget, and ongoing maintenance owner.

## 11. Current Status

- GitHub repository and initial project documentation are in place.
- Next.js, React, TypeScript, and Tailwind CSS are the selected frontend foundation.
- The local Next.js starter has been created; its complete source still needs to be reviewed, tested, and committed.
- UI implementation is intentionally pending the business's reference design and confirmed content.
- Backend and database decisions remain open.

---

**Guiding principle:** Build the smallest reliable website that makes it easy for customers to understand NK Bag House and submit a useful enquiry. Add operational complexity only when the business needs it.
