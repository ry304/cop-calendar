# COP Eligibility Calendar

A web tool for Federal Workers' Compensation case managers to track **Continuation of Pay (COP)** eligibility deadlines for traumatic injury claims.

## What it does

Enter two dates and the calendar populates automatically:

- **Date of injury** â starts the clock on all deadlines
- **First date of time loss** â determines COP eligibility

The tool calculates and highlights:

| Highlight | Meaning |
|-----------|---------|
| ðµ Blue | Date of injury |
| ð¢ Green | First date of time loss |
| ð¡ Amber | COP period (45 days from first time loss) |
| ð´ Red | Day 30 filing deadline (traumatic injury must be filed within 30 days) |
| ð  Orange | Day 45 time-loss deadline (time loss must begin within 45 days of injury) |

The tool also shows an eligibility status badge and warns if the employee does not qualify for COP.

## Export

Click **Export to PDF** to download a dated, printable calendar â named automatically with the injury date (e.g. `COP_Calendar_20260610.pdf`).

## Rules tracked

- Employee must file a traumatic injury claim **within 30 days** of injury
- Employee must begin losing time from work **within 45 days** of injury
- COP covers up to **45 calendar days** of wage loss beginning from the first day of time loss

## Tech stack

- Pure HTML, CSS, and JavaScript â no framework, no build step
- [jsPDF](https://github.com/parallax/jsPDF) for PDF export
- [Tabler Icons](https://tabler.io/icons) for UI icons

## Deployment

This is a static single-file app. Deploy to any static host:

- **Vercel** â connect GitHub repo, auto-deploys on push
- **Netlify** â drag-and-drop `index.html` or connect GitHub
- **GitHub Pages** â enable in repo Settings â Pages

## Local development

No build step needed. Just open `index.html` in a browser:

```bash
git clone https://github.com/YOUR_USERNAME/cop-calendar.git
cd cop-calendar
open index.html
```

## For internal use only

This tool is intended for internal case management use. It does not store any data â all calculations happen in the browser.
