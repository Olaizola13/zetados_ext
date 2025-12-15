# ZetaDos Privacy Policy (Code-Linked)
Last updated: 2025-12-15

This policy describes how ZetaDos (“we”, “us”, the “Platform”) processes personal data across our mobile apps and APIs. References to features and safeguards map to the code in our backend (`backend/app`) and frontend (`frontend/lib`).

## 1) Data We Collect
- **Account & identity:** email, username/display handles, profile details, photos, preferences, and consent settings (`users` collection, `ConsentPreferences`).
- **Events & routes:** event metadata you submit (titles, descriptions, schedule, sport, visibility, optional `location`, `route.polyline`, waypoints, saved route ids) as defined in `backend/app/models/event_models.py`. Polylines and waypoints are user-provided; we do not curate or verify them.
- **Location:** exact coordinates are ingested when you set event locations or use discovery. See “Location privacy & obfuscation.”
- **Reputation & enforcement:** karma votes, weights, reasons, scores, suspensions/blocks (`karma_votes_collection`, `users.karma`, `relationship_filters`).
- **Notifications & devices:** push tokens, app version, and basic telemetry needed to deliver messages and maintain sessions.
- **Integrations:** data you authorize from connected services (e.g., Strava) and the tokens required to keep them active.

## 2) How We Use Data
- Provide and secure the service: account auth, event lifecycle, invitations, confirmations, post-event feedback, and reputation scoring (`karma_service.py`).
- Show relevant events and routes: match by sport/filters and compute proximity.
- Notify you: transactional messages (invites, confirmations, reminders) and optional marketing/analytics only if you opt in.
- Integrity and safety: apply automated reputation and suspension filters to limit abuse (`karma_service.py`, `relationship_filters.py`).
- Legal: fulfill requests, meet legal obligations, and enforce Terms.

## 3) Location Privacy & Obfuscation (GDPR transparency)
- We process your exact location for matching and distance calculations, but only store/display an obfuscated version to other users when `hide_exact_location` is enabled on public events.
- Obfuscation is deterministic “jitter/fuzzing” in `backend/app/services/location_privacy.py`: exact coordinates are replaced with a seeded offset (50–200m) and a 200m radius hint; the raw `location` is withheld from non-participants. Creators and accepted participants within ~2 hours of start may see exact coordinates; others see only the obfuscated hint.

## 4) Legal Bases
- Contract: to deliver core functionality you request (events, messaging, routing, discovery).
- Consent: location access, optional marketing emails, and analytics toggles (defaults off for non-essential scopes).
- Legitimate interests: fraud/abuse prevention, service reliability, security, and aggregated analytics, balanced against your rights.
- Legal obligation: compliance with applicable laws and enforcement of Terms.

## 5) Sharing
- **Processors:** cloud hosting, Firebase services (Auth, Messaging, Analytics/Performance), storage, email/push providers, and map/places APIs (e.g., Google Maps).
- **Integration partners:** only when you connect them (e.g., Strava tokens/activity data).
- **Compliance/safety:** to comply with law or protect rights, property, and safety. We do not sell personal data.

## 6) Retention
- Data is kept while your account is active and as needed for service, dispute resolution, security, and legal obligations.
- On deletion requests, we remove or anonymize data unless retention is required by law or for ongoing disputes.

## 7) Automated Decisions & Reputation
- Karma scores and suspensions are automated from peer/system votes and relationship filters (`karma_service.py`, `relationship_filters.py`). These decisions can affect visibility, joining events, and account access. See Terms for the waiver related to automated reputation/bans.

## 8) Your Rights & Controls
- Access, correction, deletion, portability, objection (where applicable).
- Consent controls: in-app toggles for marketing/analytics, device settings for location/notifications, and disconnect integrations at any time.
- Exercise rights by emailing **hoysolozetados@gmail.com** or using in-app flows (`/users/me/consent`, data export/delete mailto links).

## 9) Security
- TLS in transit, scoped access controls, and monitoring. No system is perfectly secure; report issues promptly.

## 10) Children
- Not directed to children under 16 (or as required by local law). Contact us to remove data if you believe a child has used the service.

## 11) Changes
- We will update this policy as code or legal requirements change. Continued use after updates means you accept the revised policy.

## Contact
Questions or requests: **hoysolozetados@gmail.com**.
