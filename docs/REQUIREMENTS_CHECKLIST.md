# NK Bag House — Requirements Checklist

Use this checklist to confirm business decisions before implementation. Items marked **Pending** are questions to resolve with the business; they are not assumed features.

## 1. Business identity and content

- [ ] Confirm the approved business name and spelling.
- [ ] Obtain the final logo and any brand assets.
- [ ] Confirm the tagline and approved business description.
- [ ] Confirm the business address and service area, if they should be public.
- [ ] Confirm the phone number, WhatsApp number, and business email to publish.
- [ ] Confirm which languages the website should support.
- [ ] Obtain approved manufacturing, facility, and product photographs.

## 2. Product catalogue

- [ ] List the actual product categories.
- [ ] Confirm product names and customer-facing descriptions.
- [ ] Confirm which specifications can be published (for example, dimensions, material, capacity, colour, and construction).
- [ ] Confirm available customisation options.
- [ ] Confirm minimum order quantities for each product, if they vary.
- [ ] Decide whether prices are public, indicative, or enquiry-only.
- [ ] Identify products that should be featured on the home page.
- [ ] Confirm who will provide and approve product updates.

Do not publish example specifications as real product facts. Use the product content template in `PRODUCT_CONTENT_TEMPLATE.md` to gather verified information.

## 3. Enquiry workflow

- [ ] Confirm whether customers can enquire about a listed product, a custom product, or both.
- [ ] Agree on required fields: customer name, phone, email, quantity, and requirement details.
- [ ] Decide whether business name and delivery location are optional fields.
- [ ] Decide whether customers may attach reference images or documents.
- [ ] If uploads are allowed, set accepted file types, maximum file size, and retention period.
- [ ] Confirm who receives new enquiries.
- [ ] Choose the notification channel (for example, email or an agreed business messaging workflow).
- [ ] Decide how the business will track enquiry status and follow up.
- [ ] Define the confirmation message shown after a successful submission.
- [ ] Define how failed submissions and spam will be handled.

## 4. Website experience

- [ ] Review and approve the UI reference.
- [ ] Confirm the navigation labels and page list.
- [ ] Confirm the preferred visual direction, colours, and typography.
- [ ] Confirm the primary call to action.
- [ ] Confirm whether the site needs search, filters, or category navigation.
- [ ] Confirm whether testimonials, certifications, or client logos are available and approved for publication.
- [ ] Review mobile layouts and contact actions.

## 5. Operations and ownership

- [ ] Name the person responsible for website content updates.
- [ ] Name the person responsible for responding to enquiries.
- [ ] Agree on expected enquiry response time.
- [ ] Decide whether an admin dashboard is genuinely required for the first release.
- [ ] Confirm the domain name and who controls its registration.
- [ ] Agree on hosting and recurring budget.
- [ ] Agree on who maintains the site after launch.

## 6. Technical decisions

- [ ] Confirm the final backend choice after the enquiry workflow is understood.
- [ ] Confirm whether a database is needed for the first release.
- [ ] Confirm whether product content can initially be maintained as static content.
- [ ] Confirm whether managed image/file storage is needed.
- [ ] Define access control if private administration is introduced.
- [ ] Define data retention and deletion requirements for enquiries.
- [ ] Confirm backup, monitoring, and recovery expectations.

## 7. Release approval

- [ ] All public business details are verified.
- [ ] Product descriptions and images are approved.
- [ ] Enquiry submission has been tested end to end.
- [ ] Contact links work on desktop and mobile.
- [ ] Forms have validation, accessible labels, and clear error states.
- [ ] No secrets or private credentials are present in the repository.
- [ ] Production domain, HTTPS, and environment configuration are verified.
- [ ] Business owner has reviewed and approved the release.

---

## Decision log

Record decisions here so that implementation does not rely on assumptions.

| Date | Decision / question | Owner | Status |
|---|---|---|---|
| TBD | Final product catalogue and specifications | Business | Pending |
| TBD | Enquiry recipient and notification method | Business | Pending |
| TBD | Public pricing or enquiry-only | Business | Pending |
| TBD | Backend, database, and hosting | Project | Pending |
