# AC-34 Matiala — BLO Attendance Portal

Fresh Supabase-free attendance portal for 430 BLOs.

## Features
- BLO login by Part/PS No. + registered mobile
- Present / Absent attendance
- Current GPS capture with accuracy
- Field-working photo from device camera
- Submission timestamp
- Officer/date dashboard
- Total / Present / Absent / Pending counts
- GPS map links and photo links
- CSV export
- One production URL can be shared with all 430 BLOs

## Data
The portal is based on the uploaded `For Hearing Schedule-3.xlsx` and contains the AC-34 Matiala 430 PS/BLO master mapping.

## Shared backend
The repository is frontend-first. For central shared attendance, the included design uses Google Apps Script + Google Sheets + Google Drive instead of Supabase. Set `API_URL` in `app.js` to the deployed Apps Script Web App URL.

For official production use, move the master-data lookup/authentication behind the backend so mobile numbers are not publicly downloadable from the frontend.
