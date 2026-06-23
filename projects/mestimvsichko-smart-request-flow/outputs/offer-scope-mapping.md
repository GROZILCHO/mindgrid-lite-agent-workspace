# Strategy Output: Offer Scope Mapping

## 1. Executive Scope Summary

This document maps possible offer scope for the Mestimvsichko Smart Request Flow. It is not a final commercial offer, not a pricing document, and not an implementation task.

Current situation:

- Project-lead-reported context: Nikola / "Koleca" has reportedly seen the direction and asked for an offer.
- Confirmed repo fact: an external demo / release-candidate WordPress plugin implementation exists in `../mindgrid-request-system`.
- Confirmed repo fact: the implementation repo is on `develop`, latest relevant commit `77c64a1 merge: sprint 6 demo estimate preview into develop`, latest relevant tag `v0.6.0-rc.1`.
- Production/live status remains HOLD.
- Production execution is not approved yet.
- The next step is to map scope clearly before writing the final offer or proposing prices.

The offer should be framed as a controlled Phase 1 request-intake improvement, not as a full app, booking system, payment system, CRM, or automatic pricing platform.

## 2. Inputs Reviewed

Reviewed inputs:

- Strategy boundary output: `outputs/strategy-phase-boundary.md`
- UX flow output: `outputs/ux-bulgarian-mvp-flow-outline.md`
- Content copy output: `outputs/content-bulgarian-copy-refinement.md`
- Consolidated QA review: `outputs/qa-consolidated-mvp-review.md`
- Client/demo explanation outline: `outputs/client-demo-explanation-package-outline.md`
- Implementation repository status integration: `outputs/implementation-repository-status-integration.md`
- Current project memory: project brief, current status, decisions, tasks, issues, next actions, and agent handoff
- Known client-reported context: demo direction reportedly approved and offer requested

## 3. Current Demonstrable Demo Scope

Confirmed demo / release-candidate capabilities from the implementation repository:

- Bulgarian multi-step request flow.
- Shortcode-based frontend form using `[mindgrid_request_flow]`.
- Standard WordPress `admin-post.php` submission.
- Custom post type request creation.
- Admin request summary.
- Live demo estimate panel.
- Review estimate card.
- Server-side demo estimate recalculation.
- Computed request number format `MRS-{post_id}`.

Project-lead-reported staging context:

- Staging demo page reportedly exists at `https://staging.mestimvsichko.bg/podrobna-zayavka/`.
- The staging page reportedly uses `[mindgrid_request_flow]`.

Important boundary:

This is demonstrable demo/RC capability. It is not a production guarantee, not a confirmed live deployment plan, and not proof that all business, legal, operational, and release-readiness questions are solved.

## 4. Recommended Paid Phase 1 Scope

Recommended base Phase 1 paid scope should stay realistic and bounded:

- Finalize and harden the current detailed request flow for Mestimvsichko.
- Align Bulgarian labels, service options, helper text, and contact wording with client-approved wording.
- Confirm and stabilize request submission behavior.
- Keep admin request creation and a practical request summary.
- Decide whether the demo estimate remains as orientation-only.
- Add or adjust disclaimers around estimate, request-vs-booking, and final price expectations.
- Preserve clear submission wording such as "Изпрати запитване".
- Run basic QA and staging validation before any live move.
- Prepare for deployment to live only after human/client approval.

Phase 1 should sell the value of better request quality and faster clarification. It should not sell automation, full pricing, online booking, payment, CRM, GPS, AI, or a mobile app.

## 5. Phase 1 Clarification-Dependent Items

These items may belong in Phase 1 only if clarified, approved, and scoped before the final offer:

- Photo uploads.
- Exact upload limits, file types, file size, storage, retention, and moderation handling.
- Production estimate rules.
- Whether the estimate is orientation-only or business-approved production logic.
- Staff response workflow.
- Email notification behavior.
- Admin fields and summary refinements.
- Privacy and consent wording.
- Status handling workflow.
- Live deployment packaging and release checks.

These should not be silently included in the base offer. Each one affects cost, risk, timeline, and responsibility.

## 6. Recommended Phase 2 / Optional Modules

Recommended optional future modules:

- Payment or deposit.
- Google Maps / distance calculation.
- Calendar / booking.
- Client accounts.
- Internal dashboard / CRM.
- Advanced pricing settings.
- Upload/photo management improvements.
- Notifications / automation.
- AI-assisted request classification.
- Route or logistics features.

These are not part of base Phase 1 unless separately quoted and approved.

## 7. Explicit Out Of Scope For Base Phase 1

The base Phase 1 offer should not include these unless they are separately added:

- Online payment.
- Confirmed booking or reservation.
- Automatic real pricing.
- Google Maps integration.
- AI.
- Full CRM.
- Full mobile app.
- Customer portal.
- Calendar scheduling.
- Production-grade upload system if not approved.
- External API integrations.

Recommended scope-control wording:

> Phase 1 е подробна форма за запитване и по-добра първоначална информация. Тя не е система за автоматична крайна цена, резервации, плащания или пълна клиентска платформа.

## 8. Demo Estimate Handling Recommendation

The demo estimate feature has value for the client/demo conversation because it makes the flow feel tangible and helps explain how structured request data could support an initial orientation.

Risk:

- The visible estimate may make the client expect real pricing.
- Users may mistake an estimate range for a final offer.
- Hardcoded demo logic is not the same as business-approved pricing.

Recommended handling:

- Keep the estimate only as orientation if the client wants it in Phase 1.
- Use strong disclaimer language if it remains visible.
- Do not call it automatic final pricing.
- Do not present it as a binding offer.
- Confirm whether the estimate should stay, be removed, or be parked for Phase 2 before final offer writing.

Recommended Bulgarian wording if the estimate remains:

> Ориентировъчната оценка е само предварителна насока. Крайната цена се уточнява след преглед на заявката и разговор с екипа.

Before production pricing, clarify:

- Which factors affect price.
- Whether ranges are acceptable.
- Who approves pricing rules.
- Whether the client accepts the risk of showing an estimate.
- Whether staff will override or confirm the estimate manually.

No prices are proposed in this document.

## 9. Photo Upload Gap

Planning expected photo support because photos can help staff understand items, access, volume, and special conditions.

Current implementation repository status says there is no upload system implemented.

Offer implication:

- If uploads are included in Phase 1, they need explicit scope for file limits, formats, size, validation, storage, access, retention, and privacy handling.
- If uploads are postponed, the Phase 1 offer should explain that users can describe items and access in text, while photo upload remains a later option.

Risk:

- Uploads can increase technical, privacy, storage, security, and moderation complexity.
- The current planning copy references up to 5 images, but that expectation is not currently implemented in the repo.

Recommended decision before final offer:

- Include uploads only if the client agrees they are necessary for Phase 1 and accepts the additional scope.
- Otherwise, park uploads as a Phase 2 or add-on item.

## 10. Staff Workflow Gap

The staff response workflow is still undefined.

Open operational questions:

- Who receives requests?
- Who reviews requests?
- Who responds to the customer?
- What response time should be expected?
- Who changes request status?
- Who writes internal notes?
- Are email notifications needed?
- Is admin review enough for Phase 1?

Why this affects offer scope:

- If staff only checks WordPress admin manually, the Phase 1 offer can stay smaller.
- If staff expects email notifications, status workflows, internal assignment, or reporting, the offer becomes larger.
- If users see a response-time promise, the business process must support it.

Recommended boundary:

Do not promise automatic follow-up, staff assignment, CRM behavior, or guaranteed response time until the operational process is confirmed.

## 11. Release / Version Consistency Risk

Known version consistency risk:

- Implementation repo tag: `v0.6.0-rc.1`
- Plugin header/constants may still say `0.4.0`

Offer/release implication:

- This mismatch should be resolved or explicitly handled before stable release packaging or production deployment.
- It does not block scope mapping, but it should be visible in release-readiness notes.

Recommended offer wording should avoid promising a production-ready release until version metadata, QA, deployment packaging, and approval are handled.

## 12. Offer Structure Recommendation

Recommended structure for the future offer, without prices:

1. Base Phase 1 Package
   - Finalize the structured request flow.
   - Align Bulgarian labels and service options.
   - Stabilize submission and admin request summary.
   - Preserve request-vs-booking disclaimers.
   - Validate on staging.

2. Optional Add-ons
   - Photo uploads.
   - Email notifications.
   - Estimate hardening.
   - Admin/status refinements.
   - Live deployment packaging support.

3. Exclusions
   - Payment, booking, real automatic pricing, Maps, AI, CRM, customer portal, mobile app, and external integrations unless separately quoted.

4. Client Decisions Required
   - Estimate behavior.
   - Upload inclusion.
   - Service labels.
   - Contact methods.
   - Staff workflow.
   - Privacy/legal path.

5. Assumptions
   - Existing demo/RC plugin is the starting point.
   - Production launch remains subject to approval.
   - Client-reported approval means direction only, not final production approval.

6. Delivery/QA Notes
   - Staging validation first.
   - Human/client review before live deployment.
   - Version metadata must be corrected before stable packaging.

7. Phase 2 Roadmap
   - Optional modules and future product expansion.

## 13. Questions Before Final Offer

Questions for project lead/client:

- What exact version did Nikola/Koleca see?
- Was it the staging demo connected to `v0.6.0-rc.1`?
- What exactly did he approve as "right direction"?
- Should estimate preview remain in the paid scope?
- Should estimate be orientation-only or production logic?
- Should photo upload be included now?
- Who receives and processes requests?
- What contact methods should be supported?
- What response promise should be shown to users?
- What must be ready for launch vs what can remain demo?
- Is the offer for Phase 1 only or Phase 1 plus optional modules?
- Should Google Maps wording be removed, kept as future idea, or scoped separately?
- Should email notifications be included or postponed?
- Who approves privacy/consent wording?

## 14. Recommended Offer Positioning

Recommended positioning:

- Present the base offer as a practical request-intake improvement.
- Emphasize better inquiry quality and faster clarification.
- Avoid calling it a booking system.
- Avoid calling it an app.
- Avoid promising automatic final pricing.
- Avoid implying production execution is already approved.

If the estimate remains, possible Bulgarian positioning:

> Подробна заявка с ориентировъчна оценка

Only use this if the estimate preview remains in the paid scope and is clearly marked as non-binding.

Safer general positioning:

> Подробна заявка за преместване, транспорт и товаро-разтоварни услуги

Suggested explanatory copy:

> Клиентът изпраща по-подробно запитване, а екипът получава по-ясна информация за услугата, адресите, достъпа, вещите и предпочитания начин за контакт. Това не е потвърдена резервация и не е крайна ценова оферта.

## 15. Recommended Next Handoff

Recommended next agent: QA Audit Agent.

Recommended QA task:

Review `outputs/offer-scope-mapping.md` for:

- scope-control clarity;
- overpromise risk;
- missing offer risks;
- Phase 1 / Phase 2 separation;
- estimate handling risk;
- upload gap handling;
- staff workflow gap handling;
- version consistency risk;
- readiness to prepare a draft commercial offer after corrections, if any.

The QA review should not request implementation, prices, PHP, CSS, JavaScript, plugin work, payment, booking, AI, Maps, CRM, or production deployment.
