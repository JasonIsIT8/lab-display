# \# Computer Lab Door Display

# 

# A lightweight, self-updating door display for lab hours and manager contact info.

# Hosted free on GitHub Pages — update hours from any browser, changes appear within 60 seconds.

# 

# \---

# 

# \## How to update hours

# 

# 1\. Go to your repository on \*\*github.com\*\*

# 2\. Click on `hours.json`

# 3\. Click the \*\*pencil icon\*\* (top right of the file view) to edit

# 4\. Change any hours value — or set a day to `"Closed"`

# 5\. Scroll down and click \*\*"Commit changes"\*\*

# 6\. Done — the display refreshes automatically within 60 seconds

# 

# \### hours.json format

# ```json

# {

# &#x20; "monday":    "8:00 AM – 9:00 PM",

# &#x20; "tuesday":   "8:00 AM – 9:00 PM",

# &#x20; "wednesday": "8:00 AM – 9:00 PM",

# &#x20; "thursday":  "8:00 AM – 9:00 PM",

# &#x20; "friday":    "8:00 AM – 5:00 PM",

# &#x20; "saturday":  "10:00 AM – 4:00 PM",

# &#x20; "sunday":    "Closed"

# }

# ```

# 

# To close for a holiday, just set that day to `"Closed"`.

# 

# \---

# 

# \## Files

# 

# | File | Purpose |

# |------|---------|

# | `index.html` | The display page — runs on the tablet/screen |

# | `hours.json` | All editable data: hours, manager info, lab name |

# | `README.md` | This file |

# 

# \---

# 

# \## First-time GitHub Pages setup

# 

# 1\. Go to your repo → \*\*Settings\*\* → \*\*Pages\*\*

# 2\. Under "Source", select \*\*Deploy from a branch\*\*

# 3\. Choose \*\*main\*\* branch, \*\*/ (root)\*\* folder

# 4\. Click \*\*Save\*\*

# 5\. Your display will be live at `https://YOUR-USERNAME.github.io/lab-display/`

# 

# \---

# 

# \## Display setup (tablet or Raspberry Pi)

# 

# Open a browser, navigate to your GitHub Pages URL, and go fullscreen:

# \- \*\*Chrome / Chromebook\*\*: press `F11`

# \- \*\*Raspberry Pi kiosk\*\*: `chromium-browser --kiosk https://your-url`

# \- \*\*Android tablet\*\*: use Chrome, tap menu → "Add to Home Screen"

