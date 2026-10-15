# AI Consulting Build Log

Living copy: https://claude.ai/code/artifact/66a91604-2578-49e9-972d-6f6c61a0dd9f
(The Claude doc is the primary version. This file is the backup, updated at each milestone.)

## Purpose

Records the major steps and decisions behind each AI consulting demo so any of them can be rebuilt or explained later. When all demos are rebuilt, this log is the source for the client presentation.

## Where everything lives

| Item | Where | Status |
| --- | --- | --- |
| Shared Task Board (Demo 1) | https://claude.ai/artifact/7fMdZgCMrpq2f7Q64SJMLv | Live, private until shared |
| Email Triage demo (Demo 2) | Airtable base "Ai Email Review/Drafter Example" | Data intact, automations lost |
| Competitor Review Watch (Demo 3) | Airtable base "Competitor Review Watch" | Data intact, automations lost |
| Source code and log copy | This repo, `demos/` and `docs/` | Current |
| Portfolio page (customer-facing) | https://claude.ai/artifact/LXXQk44V64WVm8DcR1GP4x, source in `demos/portfolio/` | Private until shared |
| Inbox Assistant interface (Demo 2) | Airtable base "Ai Email Review/Drafter Example" | Published inside the base |
| Reputation Watch interface (Demo 3) | Airtable base "Competitor Review Watch" | Draft, not published |
| Recovery notes from Sept 12 | https://claude.ai/artifact/Fgd7bBtc1UZoLCYLEP2vGt | Reference only |
| Original consulting plan files | Alvin's PC: Documents\Claude Recovery, folder 6 | Not yet uploaded |

## Demo 1: Shared Task Board

Rebuilt October 2, 2026. Source: `demos/task-board/task-board.html`.

Major steps:
1. Confirmed the old tracker was gone from artifacts, Drive, and Airtable.
2. Chose a Claude artifact with shared storage over Airtable or Google Sheets: free, one link, live sync, no accounts for viewers.
3. Built the page with a shared database for tasks and board settings; nothing hard-coded.
4. Published, seeded with the rebuild tasks, verified reads at Contributor level.
5. Saved the source to this repo.

Sharing: open the board, Share, invite by email as Contributor.

Decisions: assignee is free text so outside people can be assigned; read-only visitors see an explanatory banner.

## Demo 2: Email Triage (Airtable)

Rebuilt October 15, 2026. Data was intact; automations and screens rebuilt.

Built:
- Automation 1, AI triage: new email -> AI picks Category and Priority, drafts a reply, sets Pending Review.
- Automation 2, Send approved reply: Status = Approved -> email the draft to the sender (built-in email until Gmail is connected), set Sent.
- Automation 3, Score chatbot leads: new lead -> AI rates Hot/Warm/Interested/Browsing and summarizes the service needed.
- Interface "Inbox Assistant": Review Queue (record review with tabs Needs my review, Urgent, Sent), Pipeline (kanban by status), Website Leads (kanban by lead status). Published.

Left to do:
1. Alvin turns on the three automations in Airtable.
2. Connect Gmail in Airtable and swap the send step.
3. Pick the real email intake (Airtable email trigger or Zapier Gmail trigger).
4. Delete two junk JSON choices from the Priority and Category fields.

## Demo 3: Competitor Review Watch (Airtable)

Rebuilt October 15, 2026, except the Google fetch (needs an API key).

Built:
- Lookup fields on Reviews: Business Name, Is My Business.
- Automation 1, Analyze new review: AI tags Sentiment and Themes; drafts an owner reply only for the client's own reviews.
- Automation 2, Monday digest: weekly cron, Monday 8am Central -> find past week's reviews -> AI writes headline and digest -> saved to Weekly Digests.
- Interface "Reputation Watch" (draft): Overview dashboard (rating trend, new reviews per week, business dropdown, recent reviews grid), Reply to Reviews (record review, tabs My business and Needs attention), Weekly Digests, Businesses Watched.

Left to do:
1. Google Places API key, then a scheduled script step writing Snapshots and Reviews.
2. Alvin turns on the two automations.
3. Add owner email to the Monday digest.
4. Publish the interface when ready to show.

## Decisions log

| Date | Decision | Why |
| --- | --- | --- |
| Oct 2, 2026 | Start with the task board | Lost completely; tracks the rest of the work. |
| Oct 2, 2026 | Task board as Claude artifact with shared storage | Free, one link, live sync, no per-seat cost. |
| Oct 2, 2026 | Log kept as Claude doc plus repo copy | Doc is easy to read and comment on; repo survives account or machine loss. |
| Oct 2, 2026 | Demos stay customer-facing, backend hidden | Original portfolio design preference. |
| Oct 15, 2026 | Portfolio presented as before/after per service, not as a tool list | Customers buy the outcome; the tools stay hidden. |
| Oct 15, 2026 | Airtable's built-in AI steps instead of a separate AI API | No extra account or key; runs inside the client's base. |
| Oct 15, 2026 | Nothing published publicly; all pages private until Alvin shares | Alvin's instruction. |

## Next up

1. Alvin: turn on the five automations (three in email base, two in review base).
2. Alvin: Google Places API key for the review fetch.
3. Alvin: upload the three consulting plan files from the PC.
4. Alvin: share the task board with employees.
5. Next demo candidates: appointment reminders, invoice follow-up (QuickBooks is connected), weekly owner report.
6. Combine demos into one presentation.
