# UGC job autopilot: setup

Three daily scheduled tasks that run in the Claude desktop app on your computer and use Claude in Chrome to apply to jobs on Billo, Insense and JoinBrands.

| Task | Prompt file | Time (Hawai'i) |
|---|---|---|
| Billo | `billo-task.md` | 3:00 AM daily |
| Insense | `insense-task.md` | 3:20 AM daily |
| JoinBrands | `joinbrands-task.md` | 3:40 AM daily |

The three tasks start 20 minutes apart so they don't fight over the same browser.

Every job gets logged to the Google Sheet **UGC Job Applications Tracker**:
https://docs.google.com/spreadsheets/d/1D7KGv8R68XPQ6_Xc1mS4maYR38zVqo4rKvplge3kgV0/edit

## One-time setup

1. Install the Claude in Chrome extension and connect it to the Claude desktop app.
2. In Chrome, sign in to Billo, Insense and JoinBrands with "remember me" checked.
3. Make sure Google Drive / Sheets is connected in Claude, so the tasks can write to the tracker.
4. In the Claude desktop app, create a scheduled task for each platform: paste the whole contents of its prompt file and set it to repeat daily at the time in the table (Hawai'i time).
5. Run each task once now, while you watch, before you leave it on its own.

## For the 3 AM runs to work

- The computer must be on and awake (turn off sleep, or set it to wake before 3 AM).
- The Claude desktop app and Chrome must be open.
- If a site logs you out or shows a CAPTCHA, that task stops and logs "Blocked". Sign back in and it will pick up the next day.

## Each morning

Open the tracker and filter Status to "Needs Alaina". Those are jobs that need a fact or decision only you can give.
