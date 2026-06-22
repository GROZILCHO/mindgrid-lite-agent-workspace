# Strategy Output: Phase 1 / Phase 2 Boundary

## Executive Summary

In Phase 1, Smart Request Flow should be a structured inquiry flow for Mestimvsichko.bg. Its job is to help private clients and small businesses explain what service they need, where it happens, what must be moved, whether photos or extra services are relevant, and how Mestimvsichko can contact them.

Phase 1 should not act like a pricing engine, booking system, payment system, AI assistant, tracking system, or CRM. It should make the first conversation with the client faster, clearer, and more useful.

## Phase 1 MVP Definition

### What Is Included

- A clear five-step request flow:
  1. Service type selection.
  2. Addresses and access conditions.
  3. Items, inventory, or description of what needs to be moved.
  4. Photos and additional services.
  5. Contact details and submission.
- Bulgarian-language field labels, helper text, and confirmation copy.
- Clear explanation that the user is submitting a request, not making a booking.
- Simple guidance that helps users provide enough details before Mestimvsichko calls or replies.
- Limited photo upload expectations, such as up to 5 images in JPG, PNG, or WebP with reasonable size limits.
- Internal request details that help the team understand the inquiry before contacting the client.

### What Problem It Solves

Many moving and transport inquiries start incomplete. Clients may forget access details, floors, elevators, parking, item volume, photos, storage needs, or contact preferences.

The Phase 1 MVP solves this by collecting the right minimum information in a guided way. It reduces unclear back-and-forth and helps Mestimvsichko qualify requests faster.

### Why It Is Useful Before Speaking With The Client

Before the first call or reply, Mestimvsichko can see:

- What service the client needs.
- Where the job starts and ends.
- Whether there are access problems.
- What type and amount of items are involved.
- Whether photos or additional services are relevant.
- Who to contact and how.

This gives the team better context without pretending the website can calculate or confirm everything automatically.

## Phase 1 Explicit Non-Promises

The MVP must not promise:

- Automatic price calculation.
- Final offer generation.
- Confirmed booking or reserved time slot.
- Online payment.
- Calendar reservation.
- GPS or live tracking.
- AI automation.
- Full CRM automation.
- Automatic dispatching or staff assignment.
- Guaranteed availability.
- Instant approval of the request.

Recommended principle: every user-facing message should say or imply "request sent for review", not "service booked" or "price confirmed".

## Phase 2 Opportunity

Phase 2 can be considered only after the Phase 1 request flow proves useful.

Possible later opportunities:

- Better internal request dashboard or status labels.
- Saved service categories and reusable form presets.
- Admin filtering by service type, location, urgency, or request status.
- Basic email templates for replying to clients.
- Optional estimate ranges based on manually maintained rules, if the business approves the risk.
- Calendar coordination or availability checks, if operationally realistic.
- Lightweight CRM-style request history.
- Integration with analytics to see where users abandon the flow.

These should remain separate from Phase 1. They are product opportunities, not MVP promises.

## Client Positioning

Use practical Bulgarian business framing with Nikola / "Колеца":

> Идеята не е сайтът автоматично да смята цена или да приема резервации. Идеята е клиентът да подаде по-пълно запитване, за да може екипът по-бързо да разбере каква услуга е нужна и да върне адекватен отговор.

Suggested explanation:

- "Това е умна форма за запитване, не система за автоматична оферта."
- "Клиентът описва услугата, адресите, достъпа, вещите, снимките и контактите си."
- "След изпращане екипът преглежда заявката и се свързва с клиента."
- "Първата версия трябва да е ясна, практична и лесна за използване."
- "По-сложни функции могат да се мислят по-късно, ако видим, че формата реално помага."

Avoid phrases such as:

- "Автоматична цена"
- "Резервирай час"
- "Потвърдена поръчка"
- "AI система"
- "CRM платформа"
- "Проследяване в реално време"

Safer wording:

- "Изпрати запитване"
- "Опиши какво трябва да се премести"
- "Ще се свържем с вас за уточнение"
- "Заявката не е потвърдена резервация"
- "Крайната цена се уточнява след преглед на информацията"

## Reusable Service Pattern

The strategic opportunity is to treat this as a reusable request-intake pattern for small service businesses.

The reusable pattern could include:

- Service type selection.
- Location and access details.
- Job-specific details or inventory.
- Photos or attachments.
- Contact and consent fields.
- Clear request-submission language.
- Admin review expectations.

This pattern could fit movers, transport providers, repair services, cleaning teams, storage providers, installation teams, and similar local service businesses.

For Phase 1, Mestimvsichko should remain the priority. Reusability should guide clean thinking, but it should not add extra screens, technical complexity, or abstract product features before the Mestimvsichko flow works.

## Strategic Risks

- Scope creep: advanced product ideas may distract from the immediate website redesign and request intake goal.
- Client expecting a full app: the concept could be misunderstood as a booking platform, CRM, or automation system.
- Request vs booking confusion: users may think they have reserved a service if the wording is too strong.
- Upload/file handling risk: photos are useful, but upload limits, formats, and file-size expectations need careful handling.
- Too much technical promise before demo value is clear: the first value should be clearer inquiries, not infrastructure or automation claims.
- Reusable pattern pressure: trying to serve every future business type could weaken the Mestimvsichko-specific MVP.

## Recommended Next Handoff

Recommended next agent: UX Design Agent.

The UX Design Agent should next create a Bulgarian MVP flow outline that defines:

- The five-step screen or section structure.
- Bulgarian field labels for each step.
- Helper text that explains what the user should enter.
- Confirmation and submission wording that avoids booking or final-offer promises.
- Where upload guidance and limits should appear.
- Which fields are essential for Phase 1 and which belong later.

The next handoff should stay at UX and content-structure level. It should not request WordPress implementation yet.
