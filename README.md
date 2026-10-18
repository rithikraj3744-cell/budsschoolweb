# BUDS Matriculation Higher Secondary School — Website Prototype

A responsive React + Vite public school website with Firebase Authentication and a protected Firestore announcements dashboard.

**Important:** This is an independent prototype, not an official school website. Photos, copy, contact details, admission policies, logos, management information, and all institutional claims require authorization and verification before publication.

## Run locally

1. Install Node.js 20+.
2. Run `npm install`.
3. Run `npm run dev` and open the printed localhost address.
4. The public site renders without Firebase configuration, using illustrative announcement content. The staff portal requires Firebase.

## Set up Firebase admin

1. Create a Firebase project and web app.
2. Enable Authentication → Email/Password and Firestore Database.
3. Copy `.env.example` to `.env` and fill in Firebase **web app** configuration values. These are public identifiers, not private service account secrets. Never put service account keys in the frontend.
4. In Firebase Console → Firestore → Rules, deploy the content of `firestore.rules`.
5. In Authentication, create an Email/Password user for an authorized school administrator.
6. Copy the user's UID. In Firestore, manually create `admins/{UID}` with boolean field `enabled: true` using the Firebase Console. Only trusted project owners should be able to do this.
7. Restart the dev server, open Staff Portal, and sign in. The admin can create, edit, and delete public announcements.

## Deploy

Run `npm run build`. Deploy the repository to Vercel as a Vite project; add the `VITE_FIREBASE_*` variables in Vercel Project Settings → Environment Variables. Do not deploy without reviewing the Firestore rules and securing admin access.

## Current scope and next steps

- Public: responsive Home, About, Academics, Campus Life, News, Admissions, Contact.
- Admin: email/password sign-in, Firestore UID allowlist, announcements CRUD.
- The enquiry form is explicitly **demo-only** and does not collect, transmit or store visitor details.
- Campus imagery is illustrative CSS art, not authentic school photographs.
- Extend the admin panel with moderated photo uploads, verified faculty profiles, admissions content and approved enquiry workflow after obtaining school permission.
- Add accessibility review, content moderation, privacy notice, anti-spam protections, backups and verified bilingual content before public launch.
