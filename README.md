# My Day

**Live:** https://mirloisme-star.github.io/rooz-man/

A personal daily planner that installs on a phone home screen (PWA). On iPhone, open the link in Safari and choose Share, then Add to Home Screen.

## Views

- **Today**
  - A day strip shows the whole day from 07:00 to 23:00, coloured by kind of work, with a now-line.
  - A Now card shows the current block, time left, what's next, and buttons that fit the block, such as +1 message during outreach or +30 min during course recording.
  - One tap ticks a block done; the ⋯ menu marks it half done or dropped.
  - Progress rings, a time-mix bar, a capacity meter, today's top 3 and today's tasks.
- **Plan.** A day-planner grid with two lanes: blocks on the left, tasks on the right, so you see which task sits in which block.
  - Drag a block to move it; drag its bottom edge to change its length. On a phone, press and hold briefly first.
  - Tap a block to edit its name, kind, time, note or status. Tap an empty spot to add a block.
  - **Place tasks** puts unplaced tasks into the first free deep, ops or buffer time. A task outside work time gets a dashed red border.
  - **Day options** reset the day, or save it as the default for that weekday.
- **Google Calendar.** Optional, set up on the Plan tab. My Day writes into its own calendar named "My Day" and leaves your other calendars alone. It needs your own OAuth Client ID (one-time setup steps are in the app) and asks only for the `calendar.app.created` and `calendar.calendarlist.readonly` scopes. Sync runs per day, or for the next 7 days, or automatically after each change while you are connected.
- **Tasks.** Add a task with an area chip (Medora, Tekanesh, Course, Life) and an estimate chip. When you finish it, log the real minutes. The **reality factor** chart shows, per area, how far your estimates run from reality, and Today's capacity is scaled by it.
- **Close day.** Energy from 1 to 5, what got in the way, tomorrow's top 3, and a strip of how the day actually went.
- **Week.** Seven days of blocks done, outreach and energy. "Copy weekly summary" puts a text summary on the clipboard for the Saturday review.

**My day fell apart** drops blocks in a fixed order: non-urgent Medora ops, then buffer, then a halved last mentee batch. Deep work, course, outreach and meetings are never dropped. Every action can be undone from the toast that appears.

## Data

Everything is stored in the browser's `localStorage` on each device. Use **Export backup** and **Import backup** on the Week tab to move data between devices. Imports are validated, and older Persian area names are converted to the English ones.

## Develop

```bash
python3 -m http.server 8000
```

Bump `VERSION` in `sw.js` after changing any file, or installed copies keep the cached build.
