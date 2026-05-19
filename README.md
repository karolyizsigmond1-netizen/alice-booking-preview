# Alice Beauty Studio — Booking Preview

A live preview of an online appointment-booking system built into a mirror of [alicebeautystudio.hu](https://www.alicebeautystudio.hu/).

The original homepage is preserved verbatim (HTML, CSS, photos, copy — all served from her CDN); a booking widget is layered on top:

- Every existing "Időpontfoglalás" / Reservio link opens the new booking modal instead of redirecting.
- A floating dark badge bottom-right launches the booking flow from anywhere.
- The booking flow is fully functional and connected to a live Google Apps Script backend.

## Live preview

→ **https://karolyizsigmond1-netizen.github.io/alice-booking-preview/**

## How it works

1. **Frontend** — vanilla HTML/CSS/JavaScript, no build step. The booking modal is a single self-contained snippet injected into the page.
2. **Backend** — Google Apps Script Web App (free, runs under the studio owner's own Google account).
3. **Storage** — Google Sheets (slots + bookings + services).
4. **Email** — Gmail / MailApp (booking confirmation + cancellation notices).
5. **Admin** — separate password-gated page served from the same Apps Script URL, lets the studio owner manage availability and view incoming bookings.

## What the customer sees

1. Click "Foglalás" → modal opens.
2. Pick a service (services + prices come from the backend, configurable from admin).
3. Pick a day on the calendar — only days with at least one free slot are clickable.
4. Pick a start time — only start times where the chosen service's full duration fits as consecutive free slots are shown.
5. Fill in name, phone, e-mail, optional note.
6. Confirm → two emails fly out (confirmation to customer, notification to owner).

## Recurring cost

0 Ft / month. Runs entirely on free tiers of Google Workspace + GitHub Pages, under the studio owner's own account.

## Repository structure

```
.
├── index.html        # mirror of alicebeautystudio.hu + injected booking widget
└── README.md
```

## License

Demo / portfolio piece. Photography and original page content © Alice Beauty Studio.
