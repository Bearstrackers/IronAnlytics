# IronAnlytics
Workout Progress Tracker
Iron Analytics
Live Dashboard: https://bearstrackers.github.io/IronAnlytics/
A beautiful, interactive workout dashboard for your 12-week strength program.
Features
6 KPI Cards: Sessions, Best 1RM, Volume, RPE, Adherence, Streak
Training Heatmap: 12-week consistency grid
Interactive Charts: Volume trends, lift progression, RPE tracking
Muscle Volume: Per-week breakdown
Lift Cards: Individual exercise tracking with sparklines
Session Details: Tabbed view of all 6 training days
Setup
1. Enable Live Sync (Optional)
The dashboard works offline with embedded data. For live sync with Google Sheets:
Open your Google Sheet in edit mode
Copy the original Sheet ID from the URL:
plain
https://docs.google.com/spreadsheets/d/THIS_IS_YOUR_ID/edit
Open index.html in a text editor
Find this section near the top of the <script> tag:
JavaScript
const CONFIG = {
  originalSheetId: '',  // <-- PASTE YOUR ID HERE
Paste your ID and save
Commit and push — GitHub Pages will auto-deploy
2. Auto-Sync Workflow
The repo includes .github/workflows/sync-and-deploy.yml which:
Fetches your sheet data every 6 hours
Commits updates automatically
Redeploys to GitHub Pages
Mobile Use
Open the live URL on your phone
Tap Share → Add to Home Screen
Use it like a native app at the gym
File Structure
Table
File	Purpose
index.html	The entire dashboard (self-contained)
.github/workflows/sync-and-deploy.yml	Auto-sync & deploy
sheet_data.csv	Fetched from Google Sheets (auto-generated)
Troubleshooting
Table
Issue	Fix
Sync button shows "Setup Required"	Paste your original Sheet ID in CONFIG.originalSheetId
Charts not loading	Check that Chart.js CDN is accessible
Mobile layout broken	Refresh page or clear browser cache
