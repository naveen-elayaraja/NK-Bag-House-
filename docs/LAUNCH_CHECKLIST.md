# NK Bag House — Website Launch Checklist

Use this checklist before making the website publicly available. A checked item should mean it has been tested, not merely configured.

## 1. Content and business approval

- [ ] Business name, tagline, and description approved.
- [ ] Phone, email, address, and messaging links verified with the business.
- [ ] Product names, images, and specifications verified.
- [ ] No placeholder text, sample products, or unverified claims remain.
- [ ] Pricing and minimum-order information reflect the approved business policy.
- [ ] Privacy and contact information are accurate.
- [ ] Business owner has approved the final content.

## 2. Functional testing

- [ ] Main navigation works on every page.
- [ ] Logo and home links navigate correctly.
- [ ] Product catalogue and product detail links work.
- [ ] Product enquiry action carries the correct product context.
- [ ] Enquiry form validates required fields.
- [ ] Invalid email, phone, quantity, and empty required fields are handled clearly.
- [ ] Server validates submitted data independently of browser validation.
- [ ] Success is shown only after the server confirms acceptance.
- [ ] Failed submissions show a useful message and do not silently disappear.
- [ ] Contact and messaging links open the intended destination.
- [ ] Any upload feature enforces approved file types and size limits.

## 3. Responsive and accessibility checks

- [ ] Check the home page at mobile, tablet, and desktop widths.
- [ ] Check catalogue cards and product detail layouts at narrow widths.
- [ ] No horizontal overflow or clipped content.
- [ ] Text remains readable and controls have usable touch targets.
- [ ] All form fields have visible labels.
- [ ] Keyboard users can reach and operate navigation, links, and forms.
- [ ] Focus indicators are visible.
- [ ] Images have appropriate alternative text.
- [ ] Colour contrast and heading order are reviewed.
- [ ] Reduced-motion preferences are respected if animations are used.

## 4. Performance and search visibility

- [ ] Product images are appropriately sized and optimized.
- [ ] Unused dependencies and assets are removed.
- [ ] Page titles and meta descriptions are written for each public page.
- [ ] Pages have meaningful headings and descriptive link text.
- [ ] Canonical URLs and sitemap are configured where appropriate.
- [ ] robots.txt does not accidentally block public pages.
- [ ] Social sharing metadata uses approved title, description, and image.
- [ ] A favicon and site identity assets are present.
- [ ] Check performance on a real mobile connection.

## 5. Security and privacy

- [ ] HTTPS is enabled for the production domain.
- [ ] Secrets are stored in deployment environment variables.
- [ ] No API keys, passwords, or private customer data are committed to Git.
- [ ] Public enquiry endpoints have spam protection and appropriate rate limits.
- [ ] Server-side input validation and safe error handling are enabled.
- [ ] File uploads, if present, are restricted and stored safely.
- [ ] Administrative routes, if present, require authentication and authorization.
- [ ] Only necessary customer information is collected.
- [ ] Privacy notice and data retention process are approved before collecting enquiries.
- [ ] Production dependencies and build output are reviewed.

## 6. Deployment and operations

- [ ] Production build completes successfully.
- [ ] Required environment variables are configured in the hosting platform.
- [ ] Domain DNS records point to the correct deployment.
- [ ] HTTPS certificate is active.
- [ ] Production pages load without console or server errors.
- [ ] Enquiry submission is tested against the production service.
- [ ] Enquiry recipient and notification delivery are verified.
- [ ] Monitoring and error reporting are configured where appropriate.
- [ ] Backup and recovery approach is documented for stored enquiry data.
- [ ] A person is assigned to monitor and respond to incoming enquiries.

## 7. Final sign-off

| Area | Reviewer | Status | Date |
|---|---|---|---|
| Business content | Business owner | Pending | TBD |
| Product catalogue | Business owner | Pending | TBD |
| Mobile and desktop review | Project | Pending | TBD |
| Enquiry workflow | Business / Project | Pending | TBD |
| Security and privacy | Project | Pending | TBD |
| Production deployment | Project | Pending | TBD |

**Launch rule:** Do not mark the site ready while enquiry delivery, contact details, or critical production checks remain unverified.
