# MindGrid Lite Agent Workspace — Operating Model v2

## 1. Purpose

MindGrid Lite Agent Workspace съществува, за да намали ръчното прехвърляне на контекст между ChatGPT, PM Assistant, Codex, Git и отделните project repos.

Основната му функция е да пази проектна памет, да дефинира граници, да подготвя handoff-и и да координира AI специалисти, без да заменя човешкото или PM решение.

Целта на v2 operating model е да премести работата от прекалено дребни micro-task вериги към по-практични batch review cycles.

## 2. What This Repository Is

Това repo е:

- control layer за AI-assisted работа;
- project memory за активни и бъдещи проекти;
- decision-support system;
- handoff system между роли;
- risk и scope tracker;
- място за структурирани outputs, review packets и operational status.

Тук се пази контекстът, който трябва да оцелее след chat сесии, tool ограничения и смяна на agent.

## 3. What This Repository Is Not

Това repo не е:

- implementation repo;
- final offer generator;
- production approval authority;
- заместител на PM Assistant;
- заместител на Project Lead решение;
- място, където трябва да живее целият project code;
- система, която сама одобрява scope, цена, срок, launch или клиентски ангажимент.

## 4. Repository Model

`mindgrid-lite-agent-workspace` съхранява project control files, памет, handoff-и, risks, tasks и outputs.

Реалният код, plugins, websites, themes, assets и deployment конфигурации живеят в отделни implementation repos. Workspace-ът ги реферира, но не ги копира вътре.

Всеки реален проект може да има папка под `projects/`, която пази operational memory и outputs за този проект.

Примерна структура:

```text
mindgrid-lite-agent-workspace/
projects/
  mestimvsichko-smart-request-flow/
    PROJECT_BRIEF.md
    CURRENT_STATUS.md
    TASKS.md
    NEXT_ACTIONS.md
    ISSUES_LOG.md
    DECISIONS_LOG.md
    AGENT_HANDOFF.md
    outputs/

separate repo: mindgrid-request-system/
separate repo: mall-agro-redesign/
separate repo: dorostol_trade_website/
```

Implementation repos се проверяват чрез Git, файлове, staging, build/test results и други твърди факти. Workspace-ът записва резултата от тази проверка, но не става самият implementation repo.

## 5. Source of Truth Levels

### Level 1: Hard Facts

Това са факти от repo, Git, staging, файлове, tags, commits, client-visible demos, screenshots, logs, builds или реални artifacts.

Примери:

- текущ branch;
- последен commit/tag;
- дали файл съществува;
- какво реално е имплементирано;
- какво се вижда на staging.

### Level 2: Project Lead Reported Context

Това е информация, докладвана от Project Lead, но не задължително доказана от repo или artifact.

Примери:

- клиентът е видял demo;
- клиентът е казал, че посоката е правилна;
- поискан е offer;
- production е HOLD.

Този контекст е важен, но трябва да се маркира като reported context, когато не е hard fact.

### Level 3: Agent Analysis

Това са препоръки, QA findings, strategy framing, UX suggestions, content proposals, technical briefs и scope mappings.

Agent analysis не е решение. Тя е input за решение.

### Level 4: Final Human / Project Lead Decision

Това е explicit approval от human / Project Lead.

Само това ниво може да одобри:

- final offer;
- pricing;
- production execution;
- client commitment;
- delivery scope;
- schedule;
- publication, deployment или commit/push, когато е поискано одобрение.

## 6. Role Model

### Project Lead Agent

Може да:

- приема request;
- дефинира scope;
- избира следващ agent;
- поддържа project direction;
- формулира approval gates.

Не трябва да:

- измисля client approval;
- прескача human approval;
- превръща analysis в decision без потвърждение.

### Strategy Agent

Може да:

- изяснява цели;
- дефинира Phase 1 / Phase 2 граници;
- подготвя offer scope mapping;
- формулира decision options;
- контролира overpromise risk.

Не трябва да:

- пише final commercial offer без approval;
- определя цени;
- одобрява production;
- разширява scope самостоятелно.

### UX Design Agent

Може да:

- структурира user flows;
- дефинира labels, helper text, user states и flow logic;
- открива usability risks;
- подготвя UX briefs.

Не трябва да:

- обещава функции, които не са approved;
- решава business scope;
- дава legal/privacy final wording.

### Content SEO Agent

Може да:

- подготвя user-facing copy;
- уточнява microcopy;
- предлага SEO placement notes;
- пази request-vs-booking език.

Не трябва да:

- пише binding offer language;
- обещава final price, booking, payment, AI, CRM или production features;
- дава legal claims.

### Technical Agent

Може да:

- проверява implementation repos;
- подготвя technical briefs;
- дефинира implementation constraints;
- изпълнява scoped code tasks, когато са одобрени.

Не трябва да:

- започва production implementation без approval;
- променя scope;
- решава commercial tradeoffs;
- deploy-ва без human approval.

### QA Audit Agent

Може да:

- проверява outputs;
- търси contradictions, gaps, risks и overpromise;
- валидира acceptance criteria;
- препоръчва corrections.

Не трябва да:

- одобрява final business decision;
- заменя Project Lead approval;
- поправя файлове в review-only mode.

### Documentation Agent

Може да:

- обновява Markdown memory;
- синхронизира current status, tasks, risks и handoffs;
- подготвя concise summaries;
- пази decisions отделно от recommendations.

Не трябва да:

- добавя непотвърдени approvals;
- затваря unresolved risks без основание;
- превръща planning output в final decision.

### PM Assistant

Може да:

- review-ва offer scope;
- оценява commercial risk;
- помага с project management framing;
- тълкува sprint/project implications;
- контролира client expectations;
- подпомага final offer preparation.

Не трябва да:

- получава хаотичен raw context;
- бъде третиран като автоматичен approval authority;
- замества Project Lead decision, освен ако Project Lead изрично приеме препоръката.

### Codex

Може да:

- създава и редактира файлове;
- inspect-ва repos;
- изпълнява scoped implementation tasks;
- подготвя structured outputs;
- прави file-based QA.

Не трябва да:

- решава pricing;
- пише final commercial offers;
- одобрява production;
- expand-ва scope;
- твърди client approval;
- заменя PM Assistant или Project Lead decisions.

### ChatGPT 5.5 Strategic Chat

Може да:

- действа като high-level reviewer;
- координира thinking между roles;
- challenge-ва assumptions;
- помага за strategy, framing и critical review;
- подготвя по-ясни packets за Codex или PM Assistant.

Не трябва да:

- бъде единствен source of truth;
- замества Markdown memory;
- приема agent analysis като decision;
- одобрява business commitments без human.

## 7. Codex Boundary

Codex е file/repo worker. Той е силен при ясни inputs, approved files и конкретни stop conditions.

Codex може:

- да създава и редактира файлове;
- да inspect-ва repos;
- да изпълнява scoped implementation tasks;
- да подготвя structured outputs;
- да прави file-based QA;
- да сравнява project memory с реално repo състояние.

Codex не трябва:

- да решава pricing;
- да пише final commercial offers;
- да одобрява production;
- да expand-ва scope;
- да твърди client approval;
- да заменя PM Assistant review;
- да заменя Project Lead decision;
- да превръща planning output в business commitment.

## 8. PM Assistant Boundary

PM Assistant е външен project/commercial review role.

PM Assistant review е подходящ за:

- offer scope;
- commercial risk;
- project management;
- sprint interpretation;
- client expectation control;
- final offer preparation support.

PM Assistant трябва да получава concise review packets, не raw project chaos.

Добър PM Assistant packet включва:

- текущ status;
- hard facts;
- reported client context;
- key risks;
- scope options;
- open questions;
- decisions needed;
- clear boundary: това е input, не final approval.

## 9. Batch Review Cycle

Предпочитаният workflow вече е:

```text
Input Packet -> Consolidated Agent Work -> PM/QA Review -> Correction Pass -> Memory Sync -> Commit
```

### 1. Input Packet

Project Lead или Strategy Agent подготвя ясен пакет:

- project context;
- input files;
- allowed actions;
- forbidden actions;
- expected output;
- stop conditions.

### 2. Consolidated Agent Work

Един agent или малка група agents вършат по-голям блок работа наведнъж.

Целта е да се намали цикълът:

```text
Task -> QA -> commit -> sync -> QA -> commit -> next task
```

Този micro-chain създава контрол, но прекалено много ръчна работа.

### 3. PM/QA Review

QA Audit Agent или PM Assistant review-ва целия batch output, не всяка дребна стъпка отделно.

### 4. Correction Pass

Поправят се само реалните issues. Не се стартира нова верига от несвързани tasks.

### 5. Memory Sync

Documentation Agent обновява project memory веднъж след приетия batch.

### 6. Commit

Един commit затваря batch-а след review и memory sync, когато human разреши commit.

Batch mode трябва да се използва за:

- strategy work;
- UX/content packages;
- offer preparation inputs;
- non-production planning;
- project memory consolidation;
- QA на група outputs;
- PM Assistant packets.

## 10. When Micro-Task Chains Are Still Allowed

Micro-task chains остават позволени, когато рискът изисква по-тясна проверка.

Използвай micro-task chain за:

- production code;
- WordPress plugin changes;
- deployment;
- payment;
- user data;
- client-facing final offer;
- legal/privacy wording;
- destructive repo actions;
- anything that can break live systems or create binding commitments.

При тези случаи granular QA е полезна, защото цената на грешка е по-висока.

## 11. Work Packet Types

### Strategy Packet

Purpose:
Да изясни direction, scope, options и risks.

Required inputs:

- project brief;
- current status;
- decisions log;
- risks;
- relevant outputs;
- reported client context.

Expected outputs:

- strategy recommendation;
- scope boundaries;
- assumptions;
- open questions;
- recommended next handoff.

Stop conditions:

- missing approval;
- unclear client context;
- request for pricing/final offer without PM/Project Lead review;
- production decision needed.

### Implementation Packet

Purpose:
Да изпълни scoped technical work в implementation repo.

Required inputs:

- target repo;
- branch;
- exact files/areas;
- acceptance criteria;
- forbidden actions;
- test/build expectations;
- rollback or review boundary.

Expected outputs:

- file changes;
- verification results;
- known risks;
- git status.

Stop conditions:

- unclear scope;
- production/live impact;
- payment/user data/legal risk;
- missing approval for destructive or deployment action.

### PM Review Packet

Purpose:
Да даде на PM Assistant чист, кратък материал за commercial/project review.

Required inputs:

- hard facts;
- reported context;
- scope options;
- risks;
- open questions;
- decision points.

Expected outputs:

- PM questions;
- commercial concerns;
- offer structure feedback;
- project management risks;
- recommendation for Project Lead.

Stop conditions:

- raw unfiltered context;
- missing production boundary;
- missing pricing boundary;
- unclear client approval status.

### Decision Packet

Purpose:
Да подготви explicit human/Project Lead decision.

Required inputs:

- options;
- tradeoffs;
- risks;
- recommended option;
- consequence of no decision.

Expected outputs:

- decision request;
- clear approval wording;
- decision owner;
- impact on tasks and memory.

Stop conditions:

- missing authority;
- decision affects pricing, offer, production, client commitment, legal/privacy, or deployment.

### QA Packet

Purpose:
Да провери outputs или changes срещу criteria.

Required inputs:

- reviewed files;
- context files;
- criteria;
- expected output format;
- review-only or edit mode.

Expected outputs:

- verdict;
- findings;
- risks;
- recommended corrections;
- commit recommendation.

Stop conditions:

- review-only mode with requested edits;
- missing target file;
- unclear source of truth.

### Memory Sync Packet

Purpose:
Да обнови durable Markdown memory след приет batch.

Required inputs:

- accepted outputs;
- QA verdict;
- decisions, if any;
- open risks;
- next action.

Expected outputs:

- updated current status;
- updated tasks;
- updated risks;
- updated next actions;
- updated handoff.

Stop conditions:

- output not accepted;
- unresolved QA correction;
- no clear next action;
- attempt to record recommendation as decision.

## 12. Project Folder Standard

Всеки project folder трябва да използва този базов стандарт:

- `PROJECT_BRIEF.md`
- `CURRENT_STATUS.md`
- `TASKS.md`
- `NEXT_ACTIONS.md`
- `ISSUES_LOG.md`
- `DECISIONS_LOG.md`
- `AGENT_HANDOFF.md`
- `outputs/`

Целта е всеки проект да може да се възстанови бързо без търсене в chat history.

## 13. Project Dashboard Standard

`CURRENT_STATUS.md` трябва да започва или да съдържа compact dashboard.

Препоръчани полета:

- Project;
- Current phase;
- Last accepted output;
- Current repo;
- Current branch;
- Last commit/tag;
- Client status;
- Production status;
- Next action;
- Blocked by;
- Top risks.

Dashboard-ът трябва да е кратък. Детайлите могат да останат в Summary, Blockers и outputs.

## 14. Decision Rules

`DECISIONS_LOG.md` съхранява само approved decisions.

Agent recommendations не са decisions.

PM Assistant review не е final approval, освен ако Project Lead explicitly го приеме.

Pricing, final offer, production approval и client acceptance изискват explicit Project Lead / human confirmation.

Когато има несигурност:

- маркирай я като assumption или reported context;
- не я записвай като decision;
- подготви Decision Packet.

## 15. Handoff Rules

Всеки handoff трябва да включва:

- From;
- To;
- Purpose;
- Input files;
- Allowed actions;
- Forbidden actions;
- Expected output;
- Stop conditions.

Handoff без forbidden actions е unsafe.

Добър handoff казва не само какво да се направи, а и какво да не се пипа, какво не е approved и къде agent трябва да спре.

## 16. Progress Definition

Progress в MindGrid Lite не се измерва с броя създадени Markdown files.

Progress означава:

- по-малко ambiguity;
- по-малко manual transfer;
- по-малко repeated explanations;
- по-ясно next action;
- по-добър risk control;
- по-малко Project Lead computer time;
- по-бързо context recovery;
- по-малко copy/paste между tools.

Ако нов файл не намалява uncertainty, не пази decision, не изяснява risk или не помага за next action, вероятно не е progress.

## 17. Daily / Session Operating Rhythm

### Start Session

Провери:

- current status;
- active risks;
- next action;
- what not to touch;
- changed files / git status;
- дали задачата е batch или micro-task.

### Work Block

Изпълни един batch task, максимум два.

Не сменяй agent role и scope без причина. Не започвай implementation, ако задачата е planning. Не прави memory sync преди output да е review-нат или приет.

### End Session

Запиши или докладвай:

- changed items;
- accepted outputs;
- open risks;
- next action;
- memory notes;
- final git status.

Ако задачата е review-only, не редактирай файлове.

## 18. Automation Direction

Следващата еволюция на системата трябва да намали copy/paste и да направи project state по-лесен за retrieval.

Желана посока:

- reusable packets за Strategy, QA, PM Review, Decision и Memory Sync;
- centralized project dashboards;
- по-малко нужда Project Lead да mediates всяка minor agent exchange;
- по-ясно разграничение между workspace memory и implementation repos;
- автоматизирано извличане на project state, когато tools позволяват;
- по-малко commits за дребни междинни състояния;
- повече review на batch outputs.

Automation не трябва да премахва approval gates. Тя трябва да премахва ръчното прехвърляне на контекст.

## 19. Core Rule

Ако системата създава повече copy/paste, повече micro-QA, повече commit cycles и повече manual transfer, процесът трябва да се опрости.
