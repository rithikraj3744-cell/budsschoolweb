# BUDS Group of Schools — Independent Website V3

This version removes outbound navigation to budsschools.com. All school navigation, galleries, admissions, and contacts remain on this independent React website. The Google Maps link, telephone links, and email link intentionally open their respective services.

## Run
1. Copy `.env.example` to `.env` and enter your EXISTING Firebase credentials. Never commit `.env`.
2. Run `npm install` and `npm run dev`.
3. Run `npm run build` before deploying to Vercel.

## Real photographs
No images were scraped or misrepresented. Obtain approved original photographs from the school and put them in `public/images/`. In `src/main.jsx`, populate `albumPhotos` with paths, e.g. `{'Graduation Day':['/images/graduation-1.jpg']}`. The gallery then displays images inside the website. Photos of identifiable students require appropriate authorization and consent.

## Firebase
The existing Firebase authentication, administrator document check, announcements and Firestore rules are preserved. Existing `.env` is not included. The gallery is currently a local-content gallery, not an admin upload module.

## Notes
The website is an independent prototype, not an official school publication. Confirm school-specific information before launch.
