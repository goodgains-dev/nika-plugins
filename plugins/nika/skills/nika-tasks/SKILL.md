---
name: nika-tasks
description: Use when the user wants Nika to do work for them — research, leads, drafts, outreach, CRM, web tasks, images or short videos, an industry playbook, or a big multi-day goal — or asks how their Nika tasks are going.
---

# Handing work to Nika

Pick the tool:

- **Research, leads, drafts, reports, CRM work** → `ask_ai_team`. Add `employee_id` from `list_ai_employees` if the user names someone.
- **Anything else in Nika** (a web task in a cloud browser, an image, a short video, a build) → `start_task`. With `where: "auto"`, Nika's router picks the right place.
- **A big outcome over hours or days** (get N customers, grow a number, run a campaign) → `start_task` with `where: "ultra"`.
- **Their industry's routines** → `list_playbooks`, then `run_playbook`.
- Add `business_id` from `list_businesses` when the work is for a specific business.

Rules:

- Tasks use the user's Nika credits. Say so when you start one.
- Anything that sends, posts, changes data or spends money waits for the user's approval in Nika (Execution). Tell them where to approve it.
- Give the user the `task_id`. Check back later with `task_status` (or `list_tasks`), not in a tight loop.
- Don't start the same task twice. If you're unsure whether it started, check `list_tasks` first.
