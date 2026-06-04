# CIT Computer Lab Door Display
 
A self-updating door display showing lab hours, manager contact info, and live staff location status. Hosted free on GitHub Pages — update anything from any browser, changes appear on the display within 60 seconds.
 
---
 
## Files
 
| File | Purpose |
|------|---------|
| `index.html` | The display page — runs on the tablet or screen |
| `hours.json` | All editable data: hours, manager info, and status |
| `README.md` | This file |
 
---
 
## How to update anything
 
1. Go to your repository on **github.com**
2. Click the file you want to edit (`hours.json` for most changes)
3. Click the **pencil icon** (top right of the file view)
4. Make your change
5. Click **"Commit changes"**
The display auto-refreshes every 60 seconds — no need to touch the screen.
 
---
 
## hours.json reference
 
```json
{
  "lab_name": "CIT Computer Lab",
  "location": "Massey Campus, Building V · Room 116B",
  "hours": {
    "monday":    "9:00 AM – 7:00 PM",
    "tuesday":   "9:00 AM – 7:00 PM",
    "wednesday": "9:00 AM – 7:00 PM",
    "thursday":  "9:00 AM – 7:00 PM",
    "friday":    "Closed"
  },
  "manager": {
    "name":           "Jason Hochmuth",
    "email":          "jhochmuth1@irsc.edu",
    "phone":          "(772) 462-7663",
    "office":         "Room 116B",
    "staff_location": "Building W · Room 214",
    "status":         ""
  }
}
```
 
---
 
## Staff location tile — how it works
 
The Staff Location tile on the display changes automatically based on three states:
 
| What the display shows | Color | When |
|------------------------|-------|------|
| **In the Lab** | 🟢 Green | Lab is open per schedule, `status` is empty |
| **Your custom message** | 🟡 Amber | Lab is open, `status` has text |
| **Gone for the Day** | 🔴 Red | Lab is closed per schedule — always overrides |
 
The closed state is automatic — you never need to update anything at the end of the day.
 
---
 
## Day-to-day: setting a mid-day status override
 
**Stepping out:**
1. Open `hours.json` → pencil icon
2. Set the `status` field to your message:
   ```json
   "status": "In a Meeting — Back at 2:00 PM"
   ```
3. Commit changes
**Back in the lab:**
1. Open `hours.json` → pencil icon
2. Clear the status field:
   ```json
   "status": ""
   ```
3. Commit changes
Other example status messages:
- `"At the Help Desk — Building A"`
- `"Out to Lunch — Back at 1:00 PM"`
- `"In Training — Back Tomorrow"`
---
 
## Updating hours for the week
 
Edit the `hours` section in `hours.json`. Set any day to `"Closed"` for days the lab is not open.
 
```json
"hours": {
  "monday":    "9:00 AM – 7:00 PM",
  "tuesday":   "9:00 AM – 7:00 PM",
  "wednesday": "9:00 AM – 7:00 PM",
  "thursday":  "9:00 AM – 7:00 PM",
  "friday":    "Closed"
}
```
 
> **Important:** Day names must be all lowercase (`monday`, not `Monday`). Hours values can be written however you like.
 
---
 
## Display setup (tablet or screen)
 
Open a browser, navigate to your GitHub Pages URL, and go fullscreen:
 
- **Windows / Chromebook:** press `F11`
- **Mac:** press `Control + Command + F`
- **Android tablet:** Chrome menu → "Add to Home Screen", then open and go fullscreen
- **Raspberry Pi kiosk mode:** `chromium-browser --kiosk https://your-url`
---
 
## GitHub Pages setup (first time only)
 
1. Go to your repo → **Settings** → **Pages**
2. Under "Source" select **Deploy from a branch**
3. Choose **main** branch, **/ (root)** folder
4. Click **Save**
5. Your display will be live at:
   `https://JasonIsIT8.github.io/lab-display/`
