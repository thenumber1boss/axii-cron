# axii-cron

Scheduler only. No application code or secrets live here. See `.github/workflows/cron.yml`.

Setup (about 10 minutes):
1. Create this as a **public** repository and push these files to `main`.
2. Settings > Secrets and variables > Actions > add `AXII_APP_URL` and `POLL_SECRET`
   (the same `POLL_SECRET` that is set on the Axii app in Vercel).
3. Settings > Actions > General: set "Fork pull request workflows" to require approval,
   and don't add any `pull_request` triggers.
4. Create a fine-grained token (this repo only, "Actions: read and write") and save it as `KEEPALIVE_TOKEN`.
5. Actions tab > "Axii cron" > Run workflow once. Both jobs should go green.
6. In the private Axii repo, remove the Meta poll job from `daily.yml` (the updated file is provided).