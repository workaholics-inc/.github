<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./lockup-paper.svg">
    <img src="./lockup-ink.svg" alt="Workaholics" width="360">
  </picture>
</p>

<p align="center"><b>Build things. Share them. Help each other.</b></p>

<br>

Workaholics is a small, invite-only, Persian-speaking community of people who build things: products, projects, research, startups, and things that don't have the right name yet.

It runs on one practice. Members show their work while it is still unfinished, give each other honest and specific feedback, and the owner of the work answers every piece of it.

Every Iranian student knows two sheets of paper: the چرک‌نویس, where you work things out, and the پاک‌نویس, the fair copy you hand in. Workaholics is the first sheet.

## Why

Building alone is slow. You can work on something for months and learn at the end what someone would have told you in the second week, if you had shown it to them. We don't accept that cost.

## What we hold to

**We show unfinished work.** Not once it's polished, but while it's still ugly and we aren't sure about it ourselves. This is the hardest part, and nothing else works without it.

**We give real feedback.** Empty praise helps no one. If something doesn't work, we say so. We expect that of each other; it isn't a favour.

**Trust comes before collaboration.** People find out whether they fit by seeing each other's work and how they handle a problem, not by matching skills on paper.

**Collaboration is a result, not the goal.** Shared projects and teams grow out of this. Nobody is obliged to work with anyone, and nobody is here to recruit for their own project.

**We grow slowly.** We would rather be thirty people who really see each other's work than three hundred who don't know each other's names.

None of us is a host. The founders are members like everyone else: we bring our own work into the middle and have it critiqued too.

It isn't a place to forward news, a networking group, a job board, or a room where staying silent is the default.

*None of this is meant to stay fixed. When we find that something here was wrong, we write the next version and say what changed and why.*

## How it works

- **Every piece of feedback gets an answer.** The owner replies within 7 days: *accepted*, *rejected* or *testing*, always with a reason. A reasoned no counts as much as a yes.
- **Nothing expires quietly.** An unanswered item stays visibly unanswered, with how long it has waited.
- **No scores.** No votes, likes, follower counts, karma, leaderboards or featured picks, for people, projects or feedback. Work is listed by time and by whether its feedback has been answered.
- **Your work stays yours.** Everything a member posts is members-only by default, and each owner decides what becomes public. What members achieve belongs to them; the community backs it and never claims it.
- **No money.** The platform doesn't take payments or rank anything by money.
- **The rules are public.** Every rule the platform computes is written down in [rules.md](https://github.com/workaholics-inc/storefront/blob/main/docs/rules.md), so any member can read it and propose a change.

## The code

- **[storefront](https://github.com/workaholics-inc/storefront)** (public, Apache-2.0): the website. Persian first and right to left, English second. It holds no data and no secrets; everything it shows comes from the platform's API, described by a published OpenAPI contract.
- **platform** (private): the data, the rules and the sensitive operations, such as admissions, moderation and anti-abuse. It serves the `/v1` API the storefront consumes.

The split is deliberate. What anyone can see is built in the open. Members' data stays private, and so do the abuse-prevention thresholds, since publishing them would make them useless.

TypeScript end to end: Next.js 16, Tailwind CSS 4 and next-intl on the storefront, a TypeScript API on Postgres behind it. Both are early; the storefront's [issues](https://github.com/workaholics-inc/storefront/issues) show where things stand.

## Contributing

The storefront takes contributions, and you don't need platform access to work on it: mock mode runs the site against the contract's examples. You need Node.js 24 and pnpm 12.

```bash
git clone https://github.com/workaholics-inc/storefront.git
cd storefront
pnpm install --frozen-lockfile
pnpm dev:mock
```

- Open or pick an issue first, so we agree on the approach.
- Sign off every commit (`git commit -s`) under the [Developer Certificate of Origin](https://developercertificate.org/).
- Run `pnpm gate` before you open a pull request.
- Keep the Persian and English strings in step.

Some things won't be merged however well they're built: votes, rankings or featured picks; payment or fundraising features; analytics, trackers and third-party scripts. [CONTRIBUTING.md](https://github.com/workaholics-inc/storefront/blob/main/CONTRIBUTING.md) has the full list.

Review works the way feedback works in the community: specific, honest, kind about the person and direct about the work.

Found a security problem? Please don't open an issue. Report it through [private vulnerability reporting](https://github.com/workaholics-inc/storefront/security/advisories/new).

## Joining

Membership is by invitation from an existing member. Joining is meant to be hard; it's how the group stays small enough for everyone to see each other's work.

<div dir="rtl">

## فارسی

Workaholics جمع کوچکی از آدم‌هایی است که چیزی می‌سازند: محصول، پروژه، تحقیق، استارتاپ، یا هرچیزی که هنوز اسم درستی برایش نداریم. عضویت فقط با دعوت است.

اینجا کار نصفه‌کاره را نشان می‌دهیم و بازخورد واقعی می‌دهیم. صاحب کار به هر بازخورد ظرف ۷ روز پاسخ می‌دهد: پذیرفته، نپذیرفته یا در حال امتحان، و همیشه با دلیل.

- کار نصفه‌کاره را نشان می‌دهیم
- بازخورد واقعی می‌دهیم
- اعتماد قبل از همکاری می‌آید
- از دل همین، همکاری در می‌آید
- آهسته رشد می‌کنیم

هیچ‌کدام از ما اینجا میزبان نیستیم. همه‌مان عضویم — کار خودمان را هم می‌آوریم وسط و نقد می‌شویم.

کد سایت عمومی در مخزن [storefront](https://github.com/workaholics-inc/storefront) باز است و مشارکت در آن را می‌پذیریم. راهنمای مشارکت در [CONTRIBUTING.md](https://github.com/workaholics-inc/storefront/blob/main/CONTRIBUTING.md) است.

</div>

---

<sub>The storefront's code is licensed under the Apache License 2.0. The licence doesn't cover the Workaholics name or logo; please don't present a fork as Workaholics.</sub>
