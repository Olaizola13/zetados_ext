# ZetaDos Legal (Public Mirror)

This folder is a public-ready mirror of the privacy policy and Terms of Service. Only include non-sensitive docs here.

## Files
- PRIVACY_POLICY.md (English)
- PRIVACY_POLICY_es.md (Español)
- PRIVACY_POLICY_fr.md (Français)
- PRIVACY_POLICY_de.md (Deutsch)
- TERMS_OF_SERVICE.md (English)
- TERMS_OF_SERVICE_es.md (Español)
- TERMS_OF_SERVICE_fr.md (Français)
- TERMS_OF_SERVICE_de.md (Deutsch)
- DELETE_ACCOUNT.md
- SUPPORT.md
- MARKETING.md
- COPYRIGHT
- LICENSE

## App usage
- The Flutter app loads `PRIVACY_POLICY.md` and `TERMS_OF_SERVICE.md` directly for its compliance screens. Keep the language plain and user-friendly so it reads well in-app and in this public mirror.

## Sync
- Edit files in `privacy_policy_public/` for the public/legal docs.
- Edit the root-level `SUPPORT.md`, `MARKETING.md`, `COPYRIGHT`, and `LICENSE` for those entries.
- Run `python scripts/sync_legal_mirror.py` or `make sync-legal` to update `frontend/assets/privacy_policy_public` and `assets/legal`.
- If you change policy content in `docs/PRIVACY_POLICY.md` or `docs/DELETE_ACCOUNT.md`, port the change here before syncing.

## How to publish
1. Create a new public repo and copy these files, or run:
   ```bash
   git init
   git add .
   git commit -m "Add privacy policy"
   git remote add origin <YOUR_PUBLIC_REPO_URL>
   git push -u origin main
   ```
2. (Optional) Enable GitHub Pages (Pages > Source: deploy from branch) to serve these docs publicly; update the policy with the hosted URL once you have it.
3. Link to the published URL from the app/website legal surfaces when available (privacy, terms, delete-account).
