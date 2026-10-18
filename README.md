# BUDS Group of Schools — V2

Independent demonstration website, not an official school publication.

## Run
1. `npm install`
2. Copy `.env.example` to `.env` and enter your own Firebase web app values. Never publish private service-account keys.
3. `npm run dev`
4. Open the local URL.

## Admin
Enable Firebase Email/Password authentication. In Firestore create `admins/{AUTH_USER_UID}` with Boolean `enabled: true` via Firebase Console. Publish `firestore.rules` after reviewing it. Never allow users to create their own admin record.

Announcements are filtered for all institutions, Matriculation and CBSE. School identity, contact information, admission guidance and CBSE disclosure were drawn from https://budsschools.com/. The official gallery is linked rather than copying photographs of minors.

## Notes
- This starter does not submit admission applications or upload images.
- School-specific administration roles are not implemented; approved admins can manage all announcements.
- Get authorization from school management before presenting this as an official website.
- Existing Firebase project values must be retained in your `.env`.
