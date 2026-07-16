# Swedish Mackems — Website + Sign-Up Sheet

A one-page website for the Swedish Sunderland AFC supporters branch, with a sign-up form that saves entries to a Google Sheet.

## What's in this folder

| File | What it is |
|---|---|
| `index.html` | The full website — drop this on Netlify to go live |
| `google-apps-script.js` | Paste this into Google Apps Script to connect the form to your sheet |
| `README.md` | This file |

## Setup (≈ 20 minutes)

### Step 1 — Google Sheet (5 min)

1. Go to [sheets.google.com](https://sheets.google.com) and create a blank spreadsheet
2. Name it **Swedish Mackems — Sign-Ups**
3. Add these headers in Row 1:

| A | B | C | D | E | F | G |
|---|---|---|---|---|---|---|
| Timestamp | Name | Email | Phone | City | Preferred Contact | Message |

4. Share the sheet with Stephen so you both have access

### Step 2 — Apps Script (10 min)

1. In the sheet: **Extensions → Apps Script**
2. Delete any existing code
3. Copy-paste everything from `google-apps-script.js`
4. Save (Ctrl+S), name the project anything you like
5. Click **Deploy → New deployment**
6. Gear icon → **Web app**
7. Set "Execute as" to **Me** and "Who has access" to **Anyone**
8. Click **Deploy**, authorise when prompted
9. **Copy the Web App URL** — you'll need it next

### Step 3 — Wire up the website (2 min)

1. Open `index.html` in any text editor
2. Find this line near the bottom:
   ```
   const GOOGLE_SCRIPT_URL = 'YOUR_APPS_SCRIPT_URL_HERE';
   ```
3. Replace `YOUR_APPS_SCRIPT_URL_HERE` with the URL from Step 2
4. Save the file

### Step 4 — Go live on Netlify (3 min)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag this entire folder onto the page
3. Done — you'll get a URL like `random-name-1234.netlify.app`
4. (Optional) Click **Site settings → Change site name** to get something like `swedish-mackems.netlify.app`

### Optional — Custom domain

Buy `swedishmackems.se` (or `.com`) from any registrar and point it to Netlify. Netlify has a guide for this in their dashboard under **Domain settings**.

## Things to customise

- **Email address**: search for `swedishmackems@gmail.com` in index.html and replace with your real contact email
- **Branch name**: if you settle on something other than "Swedish Mackems"
- **Cities list**: add or remove Swedish cities in the `<select>` dropdown
- **About text**: update the description to match your story
- **BLC affiliation note**: update once your registration is confirmed

## Test before sharing

1. Open `index.html` directly in a browser (just double-click it)
2. Fill in the form and submit
3. Check your Google Sheet — a new row should appear within a few seconds
4. If it works locally, deploy to Netlify and test again from the live URL
