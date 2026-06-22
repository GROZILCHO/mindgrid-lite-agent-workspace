# UX Output: Bulgarian MVP Flow Outline

## UX Summary

The Smart Request Flow should help a non-technical Bulgarian user submit a clearer service request without feeling that they are filling out a complicated business form.

The flow should feel:

- Clear: each step asks for one type of information.
- Friendly: helper text explains why the information matters.
- Practical: the user can describe the job even if they do not know exact quantities.
- Honest: the interface must make clear that this is a request, not a confirmed booking or final offer.

The Phase 1 goal is better inquiry intake for Mestimvsichko.bg, not automation.

## Step 1: Service Type Selection

### Bulgarian Step Title

Изберете услуга

### Short Helper Text

Кажете ни какъв тип помощ ви трябва, за да насочим запитването правилно.

### Recommended Service Options

- Преместване на дом
- Преместване на офис
- Транспорт на мебели или вещи
- Товарене и разтоварване
- Изнасяне на стари мебели или техника
- Складово съхранение
- Комбинирана услуга
- Друга услуга

### Other Service Handling

If the user selects "Друга услуга", show a short free-text field:

Label:

Опишете услугата

Helper text:

Напишете с няколко думи каква помощ ви е нужна.

The "other service" option should not open advanced custom logic in Phase 1. It should simply capture the request clearly for later review.

## Step 2: Addresses and Access Conditions

### Bulgarian Step Title

Адреси и достъп

### Pickup / Loading Location Fields

- Адрес за товарене
- Населено място / квартал
- Етаж
- Има ли асансьор?
- Има ли стълби или тесен вход?
- Има ли удобно място за паркиране?
- Приблизително разстояние от входа до мястото за паркиране
- Особености при достъпа

Helper text:

Тази информация помага да преценим достъпа до обекта и нужния екип.

### Delivery / Unloading Location Fields

Use these fields when the service includes delivery or moving to another address:

- Адрес за разтоварване
- Населено място / квартал
- Етаж
- Има ли асансьор?
- Има ли стълби или тесен вход?
- Има ли удобно място за паркиране?
- Приблизително разстояние от мястото за паркиране до входа
- Особености при достъпа

Helper text:

Ако има втори адрес, опишете достъпа и там. Това помага за по-точна преценка на задачата.

### Special Access Constraints

Recommended field label:

Има ли нещо важно за достъпа?

Placeholder:

Например: тесен вход, липса на асансьор, забрана за паркиране, дълъг коридор, двор, рампа, тежки врати.

## Step 3: Items / Inventory

### Bulgarian Step Title

Какво трябва да се премести?

### Recommended Inventory Categories

- Мебели
- Бяла техника
- Кашони
- Чували или багаж
- Офис оборудване
- Тежки или обемни предмети
- Чупливи предмети
- Други вещи

### Quantity / Size / Notes Guidance

Recommended fields:

- Вид на вещите
- Приблизително количество
- Размер или тегло, ако е известно
- Има ли тежки или трудни за пренасяне предмети?
- Допълнителни бележки

Helper text:

Не е нужно да знаете точни размери. Опишете вещите възможно най-практично, например "диван 3 места", "пералня", "около 20 кашона" или "голям гардероб за разглобяване".

### Low-Pressure User Guidance

Suggested microcopy:

Опишете с ваши думи. Ако не сте сигурни, напишете приблизително. Екипът ще уточни детайлите при контакт.

## Step 4: Photos and Additional Services

### Bulgarian Step Title

Снимки и допълнителни услуги

### Upload Guidance

User-facing upload text:

Можете да добавите до 5 снимки, които показват вещите, достъпа или мястото за товарене.

Accepted formats:

- JPG
- PNG
- WebP

Helper text:

Снимките помагат на екипа да прецени задачата по-точно. Не качвайте лични документи, банкови карти или чувствителна информация.

File-size guidance:

Качвайте разумно големи снимки. Ако файлът е твърде голям, може да се наложи да го намалите или да изпратите по-малко снимки.

### Additional Services / Cross-Sell Options

- Опаковане
- Разглобяване на мебели
- Сглобяване на мебели
- Изнасяне на стари мебели
- Помощ само с товарене / разтоварване
- Временно съхранение
- Почистване след изнасяне
- Друга допълнителна услуга

Helper text:

Изберете допълнителни услуги само ако са ви нужни. Ако не сте сигурни, оставете бележка и екипът ще уточни.

## Step 5: Contact and Submission

### Bulgarian Step Title

Контакти и изпращане

### Required Contact Fields

- Име
- Телефон
- Имейл, ако желаете отговор и по имейл
- Предпочитан начин за контакт
- Удобно време за връзка
- Допълнителен коментар

### Preferred Contact Method

Recommended options:

- Телефон
- Viber / WhatsApp
- Имейл
- Няма предпочитание

### Consent / Privacy Note Placeholder

User-facing placeholder:

С изпращането на запитването се съгласявате екипът на Mestimvsichko.bg да използва подадената информация, за да се свърже с вас относно заявката.

Privacy note to confirm later:

[Текстът за лични данни трябва да бъде прегледан и потвърден преди публикуване.]

### Final Submission Button Label

Изпрати запитване

Recommended confirmation text after submission:

Благодарим! Получихме вашето запитване. Екипът ще го прегледа и ще се свърже с вас за уточнение.

## Request-vs-Booking Language

Use exact Bulgarian copy like this where the user is likely to misunderstand the flow:

- Това е запитване, не потвърдена резервация.
- Изпращането на формата не гарантира свободен час.
- Крайната цена се уточнява след преглед на информацията и разговор с екипа.
- Екипът на Mestimvsichko.bg ще се свърже с вас, за да уточни детайлите.
- Ако услугата е възможна за избрания период и адрес, ще получите потвърждение от екипа.

Recommended short note near the submit button:

След изпращане ще прегледаме информацията и ще се свържем с вас. Това не е автоматична оферта или потвърдена резервация.

## Anti-Overpromise UX Copy

### Price

- Цената не се изчислява автоматично.
- Ще уточним ориентировъчна или крайна цена след преглед на заявката.
- Колкото повече детайли добавите, толкова по-точно можем да преценим задачата.

### Availability

- Изпращането на запитване не запазва час.
- Екипът ще потвърди дали има възможност за посочения период.
- Ако желаното време не е свободно, ще предложим друга възможност при контакт.

### Confirmation

- Заявката е получена за преглед.
- Услугата се счита за потвърдена само след контакт с екипа.
- Не изпращайте плащане през тази форма.

### Automation

- Формата помага да съберем нужната информация по-ясно.
- Отговорът се подготвя след преглед от екипа.
- Това не е автоматична система за оферти, резервации или проследяване.

## Admin / Internal Handling Notes

The team should receive a clear request summary that is easy to scan before calling the client.

The request should make these points easy to understand:

- Service type.
- Pickup/loading address and access details.
- Delivery/unloading address and access details, if relevant.
- Main inventory categories and approximate quantities.
- Heavy, fragile, or difficult items.
- Selected additional services.
- Uploaded photos, if any.
- Client name and contact details.
- Preferred contact method and time.
- Any notes that affect price, team size, vehicle choice, timing, or feasibility.

Staff should be able to answer these questions quickly:

- What service is being requested?
- Is there one address or two?
- Is access easy or difficult?
- Are there heavy, large, fragile, or unusual items?
- Are photos available?
- What does the client expect next?
- Is the request suitable for follow-up, or does it need clarification first?

This section defines UX/product expectations only. It does not define plugin architecture, database fields, admin screens, notification logic, or implementation details.

## Recommended Next Handoff

Recommended next agent: Content SEO Agent.

The Content SEO Agent should next refine the Bulgarian user-facing copy for:

- Step titles.
- Helper text.
- Field labels.
- Submit button and confirmation message.
- Anti-overpromise microcopy.
- Short explanation text for the request flow on the website.

The next task should keep the copy practical, friendly, and clear. It should preserve the boundary that this is a request intake flow, not a booking engine, pricing calculator, payment flow, AI tool, CRM, GPS system, or full app.

QA Audit Agent should review the flow after the Content SEO Agent produces the refined copy.
