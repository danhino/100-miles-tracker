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
- **Activity logging** — log Walk, Run, Row, or Bike entries with a date picker and +/− mile buttons (increments of 0.5)
- **Activity log** — chronological list of all entries showing date, activity type, and miles per kid
- **Stats tab** — bar chart (Chart.js) breaking down total miles by activity type, plus entry count and active days
- **Data sync** — export data as JSON for backup, import from a saved file, or clear all data
- **Dark/light mode** — automatically follows system preference
- **Mobile web app** — works as an installable PWA on iOS/Android (add to home screen)

## Usage

Open `100-miles-tracker.html` directly in any modern browser — no server or build step required.

To use across multiple devices, export your data from the **Sync** tab and save the JSON file to Google Drive or email it to yourself, then import it on the other device.

### Logging an activity

1. Set the date (defaults to today)
2. Choose an activity type: Walk, Run, Row, or Bike
3. Use the **+** / **−** buttons to set miles for Julian and/or Lauren
4. Tap **Add entry**

### Data persistence

Data is saved to `localStorage` in the browser. It persists across sessions on the same device and browser. Use **Export** to back up or transfer data.

## Tech

- Vanilla HTML/CSS/JS — no framework, no build tools
- [Chart.js](https://www.chartjs.org/) (CDN) for the activity breakdown chart
- `localStorage` for persistence
