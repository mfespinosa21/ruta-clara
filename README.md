# Ruta Clara

Fernanda Espinosa | Week 13 | Fictional referral-follow-up prototype

Live app: https://ruta-clara-pied.vercel.app/

## Current source and evidence

- `RutaClara_Week13_Source.zip` is the current Week 13 Next.js application source. Extract it; the app is in `ruta-clara-week13/`. `SOURCE.zip` is the historical Week 12 archive.
- The Week 13 archive contains `RutaClara_Week13_history.bundle`, preserving seven actual local development commits, including the packet-before-code commit and subsequent changes. The GitHub upload commits import this history as a bundle; they do not recreate its commits on this repository's main branch.
- `PACKET.md`, `IMPLEMENTATION_PROMPT.md` and `mockup-week13.png` provide the build plan and conceptual mockup; Mermaid diagrams render in the packet.
- `TEST_LOG.md` and `DECISIONS.md` record executed checks, deployment IDs, decisions and limitations.
- The Week 13 PDFs contain the packet, synthetic persona log and technical development record. BUILDCHAT is a technical record, not the complete verbatim chat export.

## Restore and run

```bash
# Restore the original development history after extracting the archive:
git clone RutaClara_Week13_history.bundle ruta-clara-history
cd ruta-clara-history
npm install
npm run dev

# Shared-rule regression checks:
node --test tests/week13.test.mjs
```

The inherited optional Supabase access requires the existing Vercel public environment settings `NEXT_PUBLIC_SUPABASE_URL` and `NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY`. Never commit private credentials or service-role keys.

## Implemented and verified

Anonymous bounded session event log and JSON export; attributed fictional evidence with step-category matching; route freshness checks; correction reopening dependent steps; conservative reverification on historical-copy load; invalid-calendar-date fix. Eight shared-rule test groups passed. Three Week 13 Vercel deployments reached READY. Browser checks demonstrated unsupported appointment-category evidence blocking attendance, explicit fictional closure and reopening from acceptance. A separate fresh-context synthetic screenshot review prompted clearer step-specific status text and was retested.

## Current limits - read before submission

The earlier GitHub write block described in historical PDFs has been resolved by uploading the Week 13 source and evidence through GitHub's web interface. Those PDFs retain their original development status; this README provides the current repository status.

The current app uses a free Vercel subdomain. A custom real domain is not connected, and the owner has declined a purchase. The supplied course rule still requires a real domain; instructor acceptance of a free subdomain has not been obtained.

Supabase email-link login is inherited. Google Sign-In remains unimplemented. Supabase RLS and ownership-policy metadata were checked; signed-in persistence and cross-account isolation were not independently retested in Week 13. The security advisor reported leaked-password protection disabled; the current UI uses email links.

Five real-user sessions (at least three strangers and no classmates), observed pain ranking and field retest/return behavior remain pending. Fictional scenarios or synthetic persona reviews do not satisfy that requirement. The student-recorded demo and full verbatim development chat remain pending. No clinical outcomes, measured savings, human validation or institutional capacity are claimed.

Academic prototype only. All clinical demo data and AI extraction outputs are fictional or simulated. Do not enter real patient data or use this prototype for care.
