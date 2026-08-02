# Assignment 2: From Idea to Launch Ready Product Plan

**Product:** TimeNova — Simple, Fast and Reliable Time Tracking for Small Businesses

\---

## Part 1: Problem Discovery and Validation

### Methods I Used

I used two of the six methods taught in class:

1. **Negative review mining** — I read Play Store and App Store reviews for QuickBooks Time and Hubstaff.
2. **Community reading** — I read Reddit threads about QuickBooks Time and Hubstaff.

**What I collected:** 3 Play Store reviews for Hubstaff, 1 Play Store review for QuickBooks Time, and 2 Reddit comments about a recent QuickBooks Time redesign. Screenshots are shown below in each section, and I explained each one in my own words.

### Competitor 1: QuickBooks Time

**What it does:** Time tracking for small and medium businesses — clock in/out, time tracking, scheduling, GPS tracking, reports, timesheets.

**What people like:** Many features, good reports, payroll connection, mobile app.

**Common problems I found:**

* Clock In/Out does not work and hours are recorded wrong (the biggest problem — this is the app's main job failing)
* Timesheets are confusing and hard to read
* The app looks worse after a recent update; too many clicks for simple tasks
* Slow loading, screens that don't respond
* Crashes, freezing, general instability
* Privacy complaint: the app kept asking for location even after work hours

**Proof I found (Play Store review + Reddit comments):**

* A 1-star Play Store review (Jordan Stone, 5/6/26) said the app used to be fast, but after a recent update it takes minutes to load and would not let him clock out. He asked the company to undo the update. This matches the Clock In/Out and slow-performance problems above.
!\[QuickBooks review — Jordan Stone](Screenshot/quickbooks-1-jordan-stone.jpeg)
* On Reddit, one user (jlenstrom) said the redesign hid the main tools inside an "apps" button and made reports feel buggier, calling it bloatware. Another reply (Nachocheeze60) said the update needs extra clicks to do simple things and complained about having to enter a "passkey" again instead of staying signed in.
!\[Reddit comment — jlenstrom / Nachocheeze60](Screenshot/quickbooks-2-reddit-jlenstrom.png)
* A second Reddit thread (Blaze\_07 / fturriaf) also said the update removed useful information from the screen, showing this is not just a one-time complaint.
!\[Reddit comment — Blaze\_07 / fturriaf](Screenshot/quickbooks-3-reddit-blaze07.png)

**Key point:** Almost all of QuickBooks Time's complaints are about its *main* job (clocking in and out correctly), not the extra features. A bug in payroll or scheduling would be annoying, but a Clock Out that quietly fails breaks trust, because it affects every employee's paycheck.

### Competitor 2: Hubstaff

**What it does:** Time tracking with employee monitoring, screenshots, activity tracking, GPS, reports, timesheets.

**What people like:** Employee monitoring, project tracking, reports.

**Common problems I found:**

* Wrong or missing time, minutes taken off, tracking stops after updates (the most common complaint)
* Having to log in again and again, other login problems
* Slow performance, freezing, app not opening
* Poor design, hard to use on mobile
* Extra charges added without permission, billing and refund problems
* Updates that bring new bugs

**Proof I found (Play Store reviews):**

* A 2-star review (Earnest Williams, 7/12/23) said he got stuck while entering the end time and could not move past it, so he uninstalled the app. This is direct proof that Clock Out fails at the exact moment it matters most.
!\[Hubstaff review — Earnest Williams](Screenshot/hubstaff-1-earnest-williams.jpeg)
* A 2-star review (Cherrie Hibaya, 7/12/25) said screenshots were not being taken on her iPad and activity showed as too low, which matters to her clients. This shows the monitoring feature is also unreliable, not just the clock.
!\[Hubstaff review — Cherrie Hibaya](Screenshot/hubstaff-2-cherrie-hibaya.jpeg)
* A 1-star review (Devin Garner, 5/8/26) said two paid add-ons were added to his account without him clicking anything or getting any notice, and he was overcharged for two years with no refund. This is direct proof of the billing problems.
!\[Hubstaff review — Devin Garner](Screenshot/hubstaff-3-devin-garner.jpeg)

**Key point:** Hubstaff focuses more on "extra" features like screenshots and activity tracking than QuickBooks Time does, and its reviews show the cost of that: the monitoring layer might work, but the basic time recording underneath does not. This shows that adding more tracking features does not fix the main reliability problem — it can even take attention away from it.

### Summary of My Research

Both apps have many features, but they share the same problem: **the main promise (recording time correctly) fails in real use**, along with slow performance, a confusing interface, and login trouble.

### What's Missing (Gap Analysis)

The problem is not a lack of features — both competitors already have too many. The real gap is **reliability and simplicity**. People just want an app that clocks in/out correctly, loads fast, does not crash, and does not force them to log in again and again.

### Is This a Painkiller or a Vitamin?

**Painkiller.** Time tracking mistakes directly cause payroll errors, pay disputes, and legal risk — this is not a "nice to have," it means real money leaving the business incorrectly every pay period. A business owner who runs payroll wrong because Clock Out didn't save has an urgent, costly problem, not a small annoyance.

\---

## Part 2: Product Definition and Tier Classification

**What TimeNova is:** TimeNova is a time tracking and attendance app for small businesses (5–100 employees) — retail shops, restaurants, and small offices — that replaces broken Clock In/Out and confusing timesheets with a fast, dependable, simple tool. Now is the right time because the big apps (QuickBooks Time, Hubstaff) have added too many features and, based on my research above, are losing user trust on the one thing that matters most: recording time correctly.

**Tier: Standard**

|Point|What I Decided|
|-|-|
|Build time|About 3 weeks — this fits Standard tier (Micro is usually a few days for one simple feature; Premium takes months and many roles)|
|Pricing model|A monthly price per employee (about $2–4/employee/month), the same way QuickBooks Time and Hubstaff already price, so buyers don't need to learn something new|
|Revenue gate|$500–1,000 in monthly revenue (around 15–30 paying small businesses) before adding Future Roadmap items like payroll connection, face recognition, or AI insights. Below that point, I will not add new features|
|Feature set|Only the core features (Clock In/Out, Timesheets, Dashboard) — no extra feature yet, because reliability itself is what makes it different, not a new capability|

**Keeping scope small:** My first Core Features list had 11 items. But based on Part 1, the real problems people complained about were only in three areas — Clock In/Out accuracy, clear timesheets, and basic speed/stability — not scheduling, GPS, or monitoring extras. So for the 3-week Standard-tier MVP, only these will be built first:

* Clock In / Clock Out (reliable, one tap, with confirmation)
* Timesheets (clean and correct)
* Basic Dashboard (shows today's attendance at a glance)

Scheduling, GPS, overtime tracking, notifications, and break tracking will come later in version 1.1, not in the launch. Building those first would repeat the same mistake I found in Part 1 — competitors adding more features on top of a core that still doesn't work well.

\---

## Part 3: Tech Stack Justification

|Part of the App|Tool I Chose|Why|
|-|-|-|
|Frontend/Framework|Next.js (React)|Fast to build alone, has a huge community, and deploys instantly on Vercel — no extra setup needed for a 3-week build.|
|Backend + Database + Login|Supabase (Postgres + built-in Login)|One tool handles the database, login, and security together — this removes the "logging in again and again" problem competitors have, since login is already well built and tested.|
|Hosting|Vercel|The free plan easily covers 0–1,000 users; deploys automatically from GitHub with no setup.|
|Payments|Stripe|The standard tool for subscription payments; avoids building a custom payment system (a proven failure point for Hubstaff, based on my research).|
|Notifications (later)|Resend or Supabase's built-in email|Added later in version 1.1, cheap to set up when needed.|

**Why this stack fits the 5 criteria:**

1. **Time to market:** Next.js + Supabase is a proven combination for solo builders; both have free plans and need no extra setup — realistic for 3 weeks.
2. **Team size and skill fit:** One person can manage this whole stack without needing a separate backend or DevOps person.
3. **Cost at 0–1,000 users:** Supabase's free plan + Vercel's free plan + Stripe (no monthly fee, only a small cut per sale) — basically $0 in fixed cost before making any revenue.
4. **How mature the tools are:** Both Next.js and Supabase have good guides, large communities, and ready-made login/payment tools — nothing needs to be built from scratch.
5. **Room to grow:** Supabase can handle tens of thousands of users on paid plans before needing any big changes; if TimeNova grows past that, moving to a bigger Postgres database is simple since it's already built on Postgres.

**What I am choosing NOT to use, and why:**

* No custom login system — Supabase's built-in login handles this, directly fixing the "logging in again and again" complaint from Hubstaff reviews.
* No custom payment system — only Stripe, matching the class idea that the real advantage is getting users, not building infrastructure.
* No native mobile app at launch (see Part 4) — this avoids app store review delays that would slow down the 3-week plan.
* No complex server setup — not needed at this size.

\---

## Part 4: Mobile App vs Web App Decision

**My decision: A web app (built as a PWA) at launch, with a native mobile app added later once revenue grows.**

1. **How people find it:** A direct link is faster to share than getting found in an app store, and this fits a 3-week timeline — no waiting for app store review.
2. **Hardware needs:** Clock In/Out does not really need special phone hardware at this stage (GPS/camera are version 1.1 features, not part of the core). A PWA can still be added to a phone's home screen so it feels like a normal app.
3. **How often it's used:** Clock In/Out happens every day, which usually favors a mobile app — but a PWA on a shared tablet at work, or on an employee's own phone browser, covers this without needing a full native app.
4. **How fast I can improve it:** A web app can be updated instantly. Since the biggest complaints from competitors were about bugs after updates, fast web updates let TimeNova fix problems the same day instead of waiting for app store approval.
5. **How it makes money:** A web app with Stripe checkout avoids the 15–30% fee app stores take — this matters at Standard-tier pricing.

**Why not build a native app first:** It would take twice as long inside a 3-week window and add app store review delays right when fast fixes matter most. A native mobile app makes sense later, once TimeNova passes the revenue gate and needs GPS or offline clock-in as special features.

\---

## Part 5: SDLC Approach

**Model: Agile (step-by-step, with room to change)**, matched to the three-part plan from class:

**1. Discover and Validate (Days 1–4)**
A one-page discovery note (not a full formal document) covering: who the user is, the main problem (Clock In/Out not working), the MVP features (Clock In/Out + Timesheets + Dashboard), and how I'll know it's working (5 small businesses using it every day).

**2. Build and Ship (Days 5–15)**
Build the MVP using Next.js + Supabase + Stripe, using AI (Claude/Copilot) to help write repetitive code, build UI parts, and write database queries so I can move fast alone.

**3. Launch and Report (Days 16–21)**
Test the app myself first → soft launch to 5–10 small businesses found through Part 6 → collect feedback through short interviews → write a closing review comparing what I built to my original plan.

**Why Waterfall would not work here:** Waterfall assumes you already know everything you need before you start, and does not allow changes once the design is locked. Since my whole idea for TimeNova (from Part 1) is that competitors' own update cycles are what broke user trust, a strict Waterfall approach would remove my ability to change direction based on real feedback — which is the exact mistake I'm trying to avoid.

\---

## Part 6: Distribution and Go-to-Market Plan

### Distribution Strategy

TimeNova is made for small businesses that want a simple, reliable time tracking tool. Instead of spending a lot of money on ads, I will focus on reaching people where small business owners already spend time online.

### Communities and Micro-Influencers

|Community / Creator|Platform|Outreach Plan|
|-|-|-|
|r/smallbusiness|Reddit|Share useful tips about employee time tracking, answer questions, and mention TimeNova when it fits the conversation.|
|r/Entrepreneur|Reddit|Join discussions about business productivity and share my product with people who are interested.|
|Indie Hackers|Community|Share my building journey, collect feedback, and find early users.|
|Mike Andes|YouTube|Reach out to him to review TimeNova and explain how it solves common time-tracking problems for small businesses.|
|Codie Sanchez|YouTube / Instagram|Reach out for a product review, since her audience is entrepreneurs and business owners.|

### Outreach Strategy

Instead of paying high sponsorship fees, I will offer creators and communities:

* Free premium access to TimeNova.
* An affiliate commission for every customer they bring in.
* Early access to new features so they can make honest reviews and demos.

This is more affordable for a new product and builds longer relationships.

### Marketing Channels

**LinkedIn**
I will post updates, product news, and short demos aimed at HR managers, startup founders, and small business owners.

**YouTube**
I will upload product demos, tutorials, and comparison videos showing how TimeNova fixes common problems like broken clock-in/out, confusing timesheets, and slow performance.

**Instagram**
I will make short reels explaining TimeNova's features, customer success stories, and time-tracking tips for small businesses.

**Reddit**
I will actively join relevant communities, answer people's questions, collect feedback, and mention TimeNova only when it adds value to the discussion.

### Why This Strategy

Small business owners usually trust recommendations from communities and creators more than regular ads. By sharing useful content, listening to feedback, and rewarding creators with affiliate commissions, TimeNova can build trust and get its first customers while keeping marketing costs low.

### If the Response Is Negative

I will treat early rejection as useful information, not failure — this is the whole point of the Launch and Report phase in Part 5. I will sort negative feedback into three types, each with its own fix:

|Type of Negative Feedback|What It Means|How I Will Respond|
|-|-|-|
|"I don't trust it yet / it's too new"|This is about trust, not the product|Offer a longer free trial, show my Part 1 research as proof the product was built to fix known problems, and offer a smaller pilot (like 1 week, 3 employees) instead of a full rollout|
|"It's missing feature X"|This may be a scope gap|Check it against Part 1 first — if X wasn't a top complaint (like GPS or payroll), it stays on the roadmap, not the MVP. I'll only move it up if several businesses ask for the same thing|
|"I tried it and Clock In/Out still felt slow or confusing"|This hits the main value of the product|This is the most serious type — I will pause outreach, fix it right away, and test again with the same business before moving to the next one, since reliability is TimeNova's whole point|

If the same negative comment comes up from 2 or more businesses, I will fix it before the public launch (Day 20 in Part 8) instead of ignoring it as a one-time comment — this keeps me true to the Agile approach instead of just following a fixed schedule no matter what.

\---

## Part 7: Success Criteria

To measure the success of TimeNova, I created the following weighted success criteria. The total weight is 100%, and each one reflects the most important goal for my product.

|Success Criteria|Weight|Reason|
|-|-:|-|
|Core features (Clock In/Clock Out, Time Tracking, Timesheets) work correctly|25%|These are the main features of TimeNova and must work reliably.|
|App performance and stability|20%|The app should load quickly, avoid crashes, and feel smooth, since these were common problems in my competitor research.|
|User interface and user experience|15%|The interface should be simple, clean, and easy to use so people can do tasks without confusion.|
|MVP completed and successfully launched|15%|The first version of the product should be finished and made available to users.|
|Real user feedback|15%|Feedback from early users will help me find ways to improve and prove the product works.|
|First 100 active users|10%|Reaching 100 active users shows that the product has real early demand.|

**Total Weight: 100%**

## Success Measurement

I will consider TimeNova successful if:

* All core features work correctly without major bugs.
* Users can clock in, clock out, and manage timesheets without errors.
* The app is fast, stable, and easy to use.
* The MVP is launched successfully.
* Early users give positive and helpful feedback.
* The product reaches at least 100 active users during the first launch period.

These success criteria focus on building a reliable product that solves the real problems I found in my competitor research, instead of just adding more features.

\---

## Part 8: Timeline (3-Week Plan)

### Week 1 — Discover and Validate

|Day|Task|
|-|-|
|1|Write the discovery note; confirm the MVP scope (Clock In/Out, Timesheets, Dashboard only)|
|2|Confirm the tier decision and revenue gate (Part 2)|
|3|Finalize the tech stack decision (Part 3)|
|4|Decide between mobile app and web app (Part 4)|
|5|Design the database structure (employees, shifts, time entries)|
|6|Sketch out the design/screens for Clock In/Out, Timesheets, and Dashboard|
|7|Set up the Next.js + Supabase + Vercel project and login system|

### Week 2 — Build Core, Payments, Stability, Outreach Prep

|Day|Task|
|-|-|
|8|Build the Clock In / Clock Out feature|
|9|Build the Timesheets screen|
|10|Build the basic Dashboard|
|11|Add Stripe subscription checkout|
|12|Test the app carefully, especially trying to break Clock In/Out, since that's the main failure point from Part 1|
|13|Fix bugs found in testing; improve the design|
|14|Research and finish the real outreach list from Part 6; send outreach messages|

### Week 3 — Launch, Feedback, Retrospective

|Day|Task|
|-|-|
|15|Soft launch to the first 5–10 businesses|
|16–17|Watch real usage and fix anything that breaks with real data|
|18|Collect feedback through short interviews (aim for 5 or more)|
|19|Improve the app based on that feedback|
|20|Public launch (through the communities in Part 6)|
|21|Write the closing review and submit the assignment|

### Rough Effort Estimate

|Week|Focus|Estimated Hours|
|-|-|-|
|1|Discover and validate|\~15|
|2|Build core + payments + stability + outreach prep|\~30|
|3|Launch + feedback + retrospective|\~15|

\---

## Reflection

I was surprised when I read the reviews for QuickBooks Time and Hubstaff. Both apps have very powerful, feature-rich offerings, yet the majority of user complaints centered on the most basic functions — Clock In and Clock Out failures, inaccurate time tracking, and confusing UI/UX design. I also noticed that a significant number of users faced repeated login issues, which added to their frustration. This showed me that having more features does not matter if the core functionality isn't reliable, which directly shaped my decision to keep TimeNova's MVP focused on getting the basics right first.

