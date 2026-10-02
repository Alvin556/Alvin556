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

Status: data intact (8 sample emails with AI drafts), automations and interface lost.

Rebuild steps (not started):
1. Decide trigger: Zapier Gmail trigger or Airtable email intake.
2. AI step to classify and draft, writing back to the record.
3. Airtable interface for approve/edit.
4. Send action that emails the approved draft.
5. Record final design and screenshot.

## Demo 3: Competitor Review Watch (Airtable)

Status: data intact (6 Gulf Shores restaurants, De Soto's marked as client), automations lost, Weekly Digests empty.

Rebuild steps (not started):
1. Confirm Google Places API key or alternative.
2. Weekly fetch as scheduled automation.
3. AI analysis step writing to Reviews.
4. Digest writer and email.
5. Interface dashboard with rating trend.
6. Record final design and screenshot.

## Decisions log

| Date | Decision | Why |
| --- | --- | --- |
| Oct 2, 2026 | Start with the task board | Lost completely; tracks the rest of the work. |
| Oct 2, 2026 | Task board as Claude artifact with shared storage | Free, one link, live sync, no per-seat cost. |
| Oct 2, 2026 | Log kept as Claude doc plus repo copy | Doc is easy to read and comment on; repo survives account or machine loss. |
| Oct 2, 2026 | Demos stay customer-facing, backend hidden | Original portfolio design preference. |

## Next up

1. Rewire Email Triage automation.
2. Rewire Competitor Review Watch automation.
3. Alvin uploads the three consulting plan files from the PC.
4. Alvin shares the task board with employees.
5. Combine demos into one presentation.
