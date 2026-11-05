# Week 13 verification record
5 November 2026 | Executed checks, fictional data only

## Mechanical failure and regression
Before changes, validDate('2026-99-01') threw RangeError: Invalid time value. Initial regression: 7 groups pass, 1 fails. After finite-date guard: 8 groups pass, 0 fail. Shared-rule checks cover calendar/leap dates, missing owner/source, overdue dates, attendance category mismatch, recorder/attestation/length limits, stale/future route, event whitelist/privacy/cap and provenance length. They do not prove every UI transition or server-side isolation.

## Browser flow actually exercised
On first publication: extraction logged event 1; eight reviewed fields allowed creation and event 2; fictional contact advance logged event 3 and progress 1/4. Unsupported next step and closure stayed disabled.
On second publication: completed fictional contact, acceptance and appointment with provenance. At attendance, appointment category blocked advance and closure. Matching attendance category plus fictional receiving confirmation allowed 4/4; explicit attendance checkbox then allowed fictional closure. Correcting acceptance reset progress to 1/4, removed dependent evidence and disabled closure. Event count reached 8. No account sign-in, real notification or clinical action was performed.

## Persona and additional observed bug
Two actual screenshots were reviewed in order by a separate fresh-context synthetic persona; a third screenshot retested the step-specific wording. The simulated reader understood contact versus institutional availability, while retaining long-copy and institutional-step coverage concerns. This is not human validation. Another mechanical finding: checked attestation could display confirmed with a mismatched category, although advancement correctly stayed blocked. Commit 60c7a00 ties status text to the same evidenceReady predicate; third deployment includes it.

## Deployment evidence - all verified READY
1. dpl_2GMtWpmE2bTvs7RW2RFRmMfisZ7b | source 6a2b7e3 | initial extension.
2. dpl_9ouVi9Hcwcr1hd2vDkRogixRCii2 | source 1878c55 | date fix and persona clarification.
3. dpl_FHkji5W3GmH2hb8FCxUwsA8K9NFZ | source 60c7a00 | final display fix.
All use existing Vercel project prj_JiFK0jXldpWsKNHa2kcATuaAyAet and alias ruta-clara-pied.vercel.app. No new application build or deployment is claimed for later document-only updates.

## Security inspection and remaining gates
Supabase metadata: referral_sessions RLS=true; authenticated ALL policy requires auth.uid()=owner_id in USING and WITH CHECK. No data rows read, no schema/policy changes. Advisor warns leaked-password protection disabled; email-link UI has no password input. Google remains unmet. No signed-in save/reload or cross-account isolation test executed this week.
GitHub import is now resolved; original development history is in its uploaded bundle. Real users, observed pain ranking/field retest/return action, matched economics, Google, real domain, full native chat export and student video remain pending. Fictional scenarios do not replace interviews.
