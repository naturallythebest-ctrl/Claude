# Enviro Pest Pathway

The master plan: phased roadmap, every project, the automated daily run, and what's needed to unblock it. Live tracker: https://claude.ai/artifact/Nq1UZAte5qJHWtooADZD7o

## Pathway

### Phase 1: Connect — this week
- **A1 Connect GorillaDesk API** (Blocked) — GorillaDesk is the hub for customers, jobs, invoices and SMS. Its API (API-key access) feeds every sync, report and auto-reply in this plan, so it comes first.  
  Next: Create an API key in GorillaDesk settings and send it to me securely. I'll test read access to customers, jobs, invoices and messages.
- **A2 Connect Stripe** (Blocked) — Reading payments and subscriptions lets us reconcile Stripe against GorillaDesk every hour and catch failed subscription charges.  
  Next: Finish connecting the Stripe connector in claude.ai (it's started but not completed).
- **A3 Link Ford Pro telematics** (Blocked) — Vehicle reporting every morning, plus an urgent alert to Robert and the team leaders if a truck is started or moved on a day off.  
  Next: In Ford Pro, turn on restricted-hours alerts for days off and add Robert and team leaders as recipients. Consider Fleet Start Inhibit.
- **A4 Clean up old project lists** (In progress) — This page replaces the scattered project lists. Collect the rules and email designs from earlier projects into one place so every automation uses the same version.  
  Next: Send me the review rules, LSA rating rules, package build rules, welcome emails and review-request emails.
- **A5 Resolve Verizon past-due bill** (Not started) — $161.51 past due on business account ending 1059-00001; service interruption was scheduled around Oct 4.  
  Next: Call 800-811-6200, confirm the balance and whether it's Frankie's old number, pay, register in My Business and turn on Auto Pay.  
  Due: Now

### Phase 2: Stabilize — weeks 2–3
- **B1 Zoho ↔ GorillaDesk two-way sync** (Not started) — GorillaDesk updates Zoho contacts and packages; Renewals statuses stay current; inactive or unhappy clients move automatically and trigger the right campaigns; Zoho edits flow back to GorillaDesk. Fix broken renewal links and tokens.  
  Next: Map fields between the two systems and list every status rule.  
  Depends on: A1
- **B2 Fix GorillaDesk communication** (Not started) — Review every field contact and repair inbound and outbound SMS, email and Rosie messages so nothing is missed.  
  Next: Audit last 30 days of GorillaDesk messages for unanswered or failed threads.  
  Depends on: A1
- **B3 Clean up email inbox and templates** (Not started) — Tidy inbox settings, rules and signatures, and build one template library in Zoho.  
  Next: Export the current Zoho email templates and mark which to keep.
- **B4 One-time and upgrade estimates** (Not started) — Add one-time and upgrade estimates to the system with email templates and payment links.  
  Next: Agree the estimate templates and price lists.  
  Depends on: A2
- **B5 Lead intake popup for Bob** (Not started) — One Zoho popup where Bob enters a new lead once; it creates the lead in Zoho and the customer and job in GorillaDesk, ready for paperwork and scheduling. Replaces the cut-and-paste sheet.  
  Next: Get a copy of Bob's current sheet and match its fields.  
  Depends on: A1
- **E1 Staff training deck** (Not started) — New slide deck covering every new program and process, built from the previous training program.  
  Next: Send me the previous training program.  
  Due: Next week
- **E2 Truck inspection training documents** (Not started) — Inspection checklist and sign-off sheet for each technician, matched to the Monday morning inspection.  
  Next: Send me the list of technicians starting next week.  
  Due: Next week

### Phase 3: Automate — weeks 3–5
- **C1 Auto-reply flow** (Not started) — Every client gets an SMS or email reply for anything in our system. Replies are chosen by request type and cover Zoho tickets and GorillaDesk SMS. Claude drafts, and Zoho Flow sends.  
  Next: Write the request types and the reply for each.  
  Depends on: A1, B2, B3
- **C2 After-hours away messaging** (Not started) — Around-the-clock acknowledgement: we received your message, we'll review it, and here are our service hours. The Sunday crew still works, but nobody has to reply right away.  
  Next: Confirm service hours and the Sunday crew schedule.  
  Depends on: C1
- **C3 Automate the daily run** (Not started) — Set up each item on the Daily run tab as a scheduled routine or workflow.  
  Next: Start with the 7 AM ticket sweep once GorillaDesk is connected.  
  Depends on: A1, A2, A3
- **C4 Review management** (Blocked) — Reply to new Google reviews based on our rules, and send review-request emails to new clients at 9 AM.  
  Next: Give manager access to the Google Business Profile.  
  Depends on: A4

### Phase 4: Grow — month 2 on
- **D1 Business budget hub** (Not started) — Real-time revenue vs. expenses for Robert and Karen, built on the budget data already in the system.  
  Next: Tell me where the existing budget data lives (QuickBooks, a spreadsheet, or both).
- **D4 Marketing plan** (Not started) — One plan across all lead sources (Local Services Ads, Google Ads, website, GorillaDesk booking, Rosie calls, referrals, email), plus a regular review of performance and local presence.  
  Next: Pull the last 90 days of leads by source.  
  Depends on: C4
- **D2 Personal budget and payment dates** (Not started) — Track personal bills and due dates, and review what can be cut.  
  Next: List recurring bills and due dates.
- **D3 Family calendar sync** (Not started) — One calendar that syncs everyone's personal and family events.  
  Next: Pick the calendar system and connect it.

## Daily run

| Time | Task | What it does | Run by | Sent to | Needs |
|---|---|---|---|---|---|
| 7:00 | LSA and leads report | Previous day's Local Services Ads and leads by location, sales and lead source, with opportunities called out. Sent by 7 AM. | Claude routine | Bob, Robert | A1, C4 |
| 7:00 | Ticket sweep 1 + vehicle report | Reconcile GorillaDesk and Zoho tickets as scheduled, completed or handled. Email Robert anything concerning. Message technicians about unresolved items (GorillaDesk inbox, Rosie). Include vehicles and driving. | Claude routine | Robert, technicians | A1, A3 |
| 7:30 | Daily company review | Budget update, upcoming wins and concerns. | Claude routine | Robert | D1 |
| 8:00 | Rate LSA leads | Rate and annotate yesterday's LSA leads based on our rules. | Claude routine |  | A4 |
| 8:30 | Review replies | Check for new reviews and reply based on our rules. | Claude routine |  | C4 |
| 9:00 | Send review requests | Send the review-request emails we already designed to new clients. | Zoho workflow | Clients | C4 |
| 10:00 | CRM flow check | Confirm GorillaDesk updates reached Zoho, Renewals statuses and stage moves are correct, campaigns triggered, and renewal links and tokens work. Push Zoho changes back to GorillaDesk. | Claude routine | Robert (exceptions only) | B1 |
| 6 AM–9 PM, hourly | Stripe ↔ GorillaDesk reconcile | Match payments, check subscription charges, flag payments not collected in the field, and QC new client intake against the package build rules. | Claude routine | Robert (exceptions only) | A1, A2 |
| 12:00 PM | Ticket sweep 2 | Same as the 7 AM sweep, without the vehicle report. | Claude routine | Robert, technicians | A1 |
| 5:00 PM | Ticket sweep 3 | Same as the 7 AM sweep, without the vehicle report. | Claude routine | Robert, technicians | A1 |
| 5:30 PM | Queue welcome emails | Line up the designed welcome emails for clients completed today, to go out the next day. | Zoho workflow | Clients | A1, A4 |
| 24/7 | Client auto-replies | Every ticket and SMS gets a reply; after hours, the away message with our service hours. | Zoho Flow + Claude | Clients | C1, C2 |
| 24/7 | Days-off vehicle alert | Urgent message if a truck starts or moves on a day off. | Ford Pro alert | Robert, team leaders | A3 |
| Mon 7:00 | Truck inspection, chemical check, 7:30 huddle | From the staff run sheet. | Staff | Technicians, manager |  |

## Needed from you

- [ ] **GorillaDesk API key** — The single biggest unlock. Without it I can't sync, reconcile, or auto-reply. (unlocks A1, B1, B2, B5, C1, C3)
- [ ] **Finish the Stripe connector** — It's started in claude.ai but not completed. (unlocks A2, B4)
- [ ] **Ford Pro admin access, and team leader names and cell numbers** — For days-off alerts and the morning vehicle report. (unlocks A3)
- [ ] **Google Business Profile and Local Services Ads access** — For review replies, review requests and the 7 AM LSA report. (unlocks C4, D4)
- [ ] **Rules and email designs from earlier projects** — Review reply rules, LSA rating rules, package build rules, welcome emails, review-request emails. (unlocks A4, C4)
- [ ] **Previous training program and the list of technicians** — For next week's training deck and inspection documents. (unlocks E1, E2)
- [ ] **Bob's current lead sheet** — So the new popup matches what he already uses. (unlocks B5)
- [ ] **Service hours and Sunday crew schedule** — For the after-hours away message. (unlocks C2)
- [ ] **Where the budget data lives** — QuickBooks is connected; tell me if there's also a spreadsheet. (unlocks D1)
- [ ] **Which calendar to use for the family calendar** — Google Calendar or Outlook. (unlocks D3)
- [ ] **Confirm whether Verizon account 1059-00001 is Frankie's old number** — So we know which line the past-due bill covers. (unlocks A5)
