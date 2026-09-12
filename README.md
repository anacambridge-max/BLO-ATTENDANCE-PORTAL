# AC-34 Matiala — 430 BLO Attendance Portal

Fresh Supabase-free source built from `For Hearing Schedule-3.xlsx`.

**430 PS/BLO records extracted from Rough Data.**

### Features
- BLO login by Part No + registered mobile
- Present / Absent
- High-accuracy GPS capture
- Camera photo capture
- Submission timestamp
- Officer/date dashboard
- Total / Present / Absent / Pending
- GPS map links and photo links
- CSV export

### Shared backend without Supabase
The included `Code.gs` uses **Google Sheets + Google Drive**:
1. Create a blank Google Sheet.
2. Extensions → Apps Script → paste `Code.gs`.
3. Run `setup()` once and authorize.
4. Deploy as Web app → Execute as Me → Who has access: Anyone.
5. Put the Web App URL into `API_URL` in `app.js`.
6. Deploy these static files to Vercel.

This lets all 430 BLOs use one public production URL; attendance/photos are stored centrally in the Google account.

**Security note:** this first build embeds master data in the frontend for simple setup. Before official production, move BLO authentication/master lookup into the Apps Script backend so registered mobile numbers are not publicly downloadable, and add a separate protected officer login.
