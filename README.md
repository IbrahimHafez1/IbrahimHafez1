# Ibrahim Hafez
**Backend Software Engineer** · Egypt · Open to remote backend roles

I build backends in TypeScript, NestJS, and PostgreSQL. At Taqdum I owned four client backends. I’m also a licensed dentist, and the appointment and follow-up workflows in my own clinic shaped how I built Intelladent.

[Explore my portfolio](https://ibrahimhafez.pages.dev/) · [Download my CV](https://ibrahimhafez.pages.dev/assets/Ibrahim-Hafez-CV.pdf) · [LinkedIn](https://linkedin.com/in/ibrahim-hafez-923307254) · [Email](mailto:ibrahimhafez24@gmail.com) · [WhatsApp](https://wa.me/201011094565)

## Selected work

**Auto Drop · Sign-in from ~6 seconds to under 1 second**

I traced the delay to bcrypt password verification. After a successful sign-in, the backend migrated the stored hash so returning users kept their passwords and subsequent sign-ins were faster. [Read the case study →](https://ibrahimhafez.pages.dev/case-studies/auto-drop-sign-in/)

**Intelladent · Managing access across clinics**

I built a multi-tenant dental platform with role-based permissions. Background jobs handle reminders and treatment follow-ups, and the waitlist can fill an appointment when a slot opens. [Explore Intelladent →](https://ibrahimhafez.pages.dev/#intelladent)

**MasrMart · Protecting seller payouts**

Order-time price snapshots preserve the amount a buyer agreed to pay. PostgreSQL advisory locks coordinate concurrent ledger updates. [Explore MasrMart →](https://ibrahimhafez.pages.dev/#masrmart)

<details>
<summary>More backend projects</summary>

- **Simbel AI** — Used a unique index to prevent duplicate campaign starts and BullMQ workers to resume interrupted campaigns. [Engineering notes](https://ibrahimhafez.pages.dev/#simbel)
- **Pupilera Admissions** — Indexed normalized Arabic and English school names for typo-tolerant search in PostgreSQL. [Engineering notes](https://ibrahimhafez.pages.dev/#pupilera)
- **The Cooking School** — Used a row lock to prevent two concurrent checkouts from booking the same remaining place. [Engineering notes](https://ibrahimhafez.pages.dev/#cooking)
- **Taqdum POS** — Built inventory, VAT, refunds, and receipt workflows for a multi-tenant point-of-sale backend.
- **EndahQR** — Built a QR-to-WhatsApp vehicle messaging backend with verified webhooks, duplicate-event handling, and durable queues.
- **Nugttah** — Designed MongoDB schemas and modernized legacy Node.js APIs for a Saudi platform. [Product](https://nugttah.com)

</details>

## Merged open-source contributions

I’ve contributed 15 merged fixes across five repositories. Three examples show how ordinary backend operations can lose data.

- **NestJS** could disconnect its Kafka producer while replies were still being serialized or sent. I made shutdown drain those replies and added a regression test against a real broker. [Review the fix · #18535](https://github.com/nestjs/nest/pull/18535)
- **Mongoose** could lose pending writes when MongoDB retried a transaction after a transient commit error. I restored document state so the retry sends the inserts and updates again. [Review the fix · #16640](https://github.com/Automattic/mongoose/pull/16640)
- **TypeORM** could delete many-to-many links during a batch save when the relation hadn’t been loaded. I fixed the regression and added a test for that case. [Review the fix · #12711](https://github.com/typeorm/typeorm/pull/12711)

<details>
<summary>Twelve more merged fixes</summary>

**NestJS Schedule and node-mssql**

- [Wait for active cron callbacks configured to finish during shutdown](https://github.com/nestjs/schedule/pull/2400)
- [Let prepared statements and transactions finish while the SQL Server pool closes](https://github.com/tediousjs/node-mssql/pull/1959)

**Mongoose**

- [Finish cursor cleanup when initialization fails or middleware skips it](https://github.com/Automattic/mongoose/pull/16612)
- [Preserve pending writes after ordered batch errors](https://github.com/Automattic/mongoose/pull/16533)
- [Wait for driver cleanup when destroying a cursor](https://github.com/Automattic/mongoose/pull/16562)
- [Surface cursor initialization errors](https://github.com/Automattic/mongoose/pull/16563)

**TypeORM**

- [Release the query runner after failed cache removals](https://github.com/typeorm/typeorm/pull/12938)
- [Release SQL Server locks after subscriber errors](https://github.com/typeorm/typeorm/pull/12939)
- [Prevent composite-key grouping collisions](https://github.com/typeorm/typeorm/pull/12905)
- [Clean up failed connection initialization](https://github.com/typeorm/typeorm/pull/12704)
- [Release query runners on CockroachDB shutdown](https://github.com/typeorm/typeorm/pull/12891)
- [Remove stale ancestor links when moving a tree branch](https://github.com/typeorm/typeorm/pull/12907)

</details>

## Tools I work with

**Backend** · TypeScript, Node.js, NestJS, Express

**Data and queues** · PostgreSQL, MariaDB, MongoDB, TypeORM, Prisma, Redis, BullMQ

**Delivery and testing** · Docker, GitHub Actions, Jest, Playwright
