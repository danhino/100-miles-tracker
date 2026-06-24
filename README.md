# 100 Miles of Summer

A mobile-friendly single-page web app for tracking the kid's summer fitness goal: 100 miles each.

## Screenshots

<table>
  <tr>
    <td align="center"><strong>Progress & Logger</strong></td>
    <td align="center"><strong>Activity Selector & Log</strong></td>
  </tr>
  <tr>
    <td><img src="screenshots/screenshot-1.jpg" width="300" alt="Progress view and activity logger" /></td>
    <td><img src="screenshots/screenshot-2.jpg" width="300" alt="Activity type selector and recent log" /></td>
  </tr>
</table>

## Features

- **Progress dashboard** — side-by-side cards showing each kid's mile count and progress bar toward 100
- **Dashboard tab** — activity overview showing active days, inactive days, and % active for each kid (calculated from configured summer start date)
- **Activity logging** — log Walk, Run, Row, or Bike entries with a date picker and +/− mile buttons (increments of 0.5)
- **Activity log** — chronological list of all entries with edit and delete buttons, showing date, activity type, and miles per kid
- **Stats tab** — individual progress bars per kid showing miles toward 100 goal, with activity breakdown by color (Walk, Run, Row, Bike). Only shows activities that kid actually logged.
- **Data sync** — export data as JSON for backup, import from a saved file, or clear all data
- **Dark/light mode** — automatically follows system preference
- **Mobile web app** — works as an installable PWA on iOS/Android (add to home screen)

## Configuration

The **Sync** tab includes a Settings section for configuring the summer start date:

- **Summer Start Date** — set via a date picker (format: YYYY-MM-DD)
- Used to calculate total active/inactive days on the Dashboard for each kid
- Stored in browser local storage alongside entry data
- Example: Set to 2026-05-28 to track from May 28, 2026 to today
- If no start date is set, the Dashboard shows a prompt to configure one

## Usage

Open `100-miles-tracker.html` directly in any modern browser — no server or build step required.

To use across multiple devices, export your data from the **Sync** tab and save the JSON file to Google Drive or email it to yourself, then import it on the other device.

### Logging an activity

1. Set the date (defaults to today)
2. Choose an activity type: Walk, Run, Row, or Bike
3. Use the **+** / **−** buttons to set miles for Julian and/or Lauren
4. Tap **Add entry**

The progress bars update instantly in both the Dashboard and Stats tabs.

### Data persistence

Data is saved to `localStorage` in the browser. It persists across sessions on the same device and browser. Use **Export** to back up or transfer data.

## Tech

- Vanilla HTML/CSS/JS — no framework, no build tools
- Custom stacked progress bars for per-kid activity breakdown
- Dynamic calculations for active/inactive days based on configurable start date
- `localStorage` for persistence
