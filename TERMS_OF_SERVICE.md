# ZetaDos Terms of Service (Code-Linked)
Last updated: 2025-12-15

These Terms govern your use of ZetaDos (“we”, “us”, the “Platform”). Feature references map to our backend (`backend/app`) and frontend (`frontend/lib`) implementations.

## 1) Account & Acceptance
By creating an account or joining/hosting events, you agree to these Terms. Use is limited to legally eligible individuals; accounts may be suspended under our automated enforcement rules.

## 2) Venue & User-Generated Routes
- Digital record only: The Platform creates and stores the event record (creator email, schedule, optional `location`, `route.polyline`, waypoints) per `backend/app/models/event_models.py`. You, the organizer, create and control the physical activity and any associated hazards.
- User-generated routes: Route polylines/waypoints are user-provided content; we only validate encoding/point counts. We do not inspect or certify terrain, traffic, legality, weather, or safety. You assume responsibility for route accuracy and on-the-ground risks.
- No venue control: We do not operate physical venues, do not supervise events, and are not liable for navigation errors, injuries, property damage, or third-party actions.

## 3) Automated Jury & Waiver
- Automated reputation: Karma and enforcement are calculated automatically from peer/system votes and weights (`backend/app/services/karma_service.py`) and from block/suspension filters (`backend/app/services/relationship_filters.py`). System votes (e.g., no-show penalties) may downrank or restrict access.
- Finality: You agree that these automated calculations and resulting suspensions/visibility limits are final for platform access decisions.
- Waiver: You waive claims, damages, or actions related to “lost reputation,” “unfair bans,” or reduced visibility resulting from these automated processes, to the fullest extent permitted by law.

## 4) Assumption of Risk (Condition to Join)
- Condition precedent: By calling or triggering the `POST /events/{id}/join` endpoint (`join_event` in `backend/app/routers/event_router.py`), you confirm you are medically and legally fit to participate.
- You assume all risks inherent in running/cycling (the only sports modeled in `SportEnum`): traffic, weather, road/route conditions, navigation errors, equipment failure, health incidents, and conduct of others. You release us from liability for such risks.

## 5) Privacy & Location Handling (Summary)
- We process your exact location for matching and distance calculations. When event creators enable `hide_exact_location` on public events, we show other users only an obfuscated center (50–200m offset) and 200m radius hint; exact coordinates are withheld unless you are the creator or an accepted participant within ~2 hours of start (`location_privacy.py`). See the Privacy Policy for details.

## 6) User Content & Conduct
- You must only post accurate, lawful content and must have rights to any data you upload (including routes and media).
- No harassment, fraud, abuse, or unsafe behavior. Violations may trigger automated downranking or suspension.

## 7) Service Changes
We may modify or discontinue features with notice when practical. Some changes may be required for security or compliance.

## 8) Disclaimers & Limitation of Liability
- The Services are provided “as is” without warranties. To the maximum extent allowed, we disclaim implied warranties of merchantability, fitness for a particular purpose, and non-infringement.
- We are not liable for indirect, incidental, special, consequential, or punitive damages, or for lost profits/reputation. Our aggregate liability is limited to the greater of (a) the amount you paid us in the last 12 months or (b) $50, except where prohibited by law.

## 9) Termination
We may suspend or terminate accounts for policy violations, abuse, or legal risk. You may stop using the Service at any time.

## 10) Governing Law
Subject to mandatory local consumer protections, governing law and venue will follow your local consumer law or, if permitted, the law of the jurisdiction where ZetaDos is established.

## 11) Contact
For questions about these Terms: **hoysolozetados@gmail.com**.
