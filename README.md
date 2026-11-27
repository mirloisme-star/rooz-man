# روز من

A personal daily planner. Persian, right-to-left, installable on a phone home screen (PWA).

- **Timeline.** Each weekday has its own block template: deep work, outreach, mentee batches, meetings, meals and buffer. You tick each block done, half done or dropped.
- **Tasks.** Each task has an area (مدورا، تکانش، دوره، زندگی) and an estimate in minutes. You log the real minutes when it is done.
- **Reality factor.** After three finished tasks in an area, the app shows how optimistic or pessimistic your estimates are. It then scales today's capacity by that factor.
- **Messy day.** One button drops blocks in a fixed order: non-urgent Medora ops, then buffer, then a shortened last mentee batch. Deep work and outreach are never dropped.
- **Close the day.** Record energy, what blocked you and tomorrow's top three. A seven-day summary can be copied to the clipboard.
- **Storage.** Data is stored in the browser's `localStorage` on each device. To move data between devices, export a backup JSON on one and import it on the other.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000. The service worker caches the app for offline use. Bump `VERSION` in `sw.js` after changing any file.

## Files

```
index.html             the whole app (HTML, CSS, JS)
manifest.webmanifest   PWA manifest
sw.js                  offline cache
fonts/                 Vazirmatn UI FD (OFL)
icons/                 app icons
```
