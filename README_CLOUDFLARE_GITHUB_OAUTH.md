# WAHA Hockey CMS on Cloudflare Pages + GitHub OAuth (Decap CMS)

This folder contains:
- admin-index.html  — drop into /admin/index.html
- admin-config.yml  — drop into /admin/config.yml (merge your collections)
- cloudflare-worker-oauth.js — a Worker that implements the GitHub OAuth proxy for Decap CMS

## 1) Create a GitHub OAuth App
- Homepage URL: https://wahahockey.org
- Authorization callback URL: https://cms-oauth.wahahockey.org/callback

## 2) Deploy the OAuth proxy on Cloudflare
- Create a **Worker** (or Pages Function) and paste `cloudflare-worker-oauth.js`
- Add **Secrets**: GITHUB_CLIENT_ID, GITHUB_CLIENT_SECRET
- Add **Vars** (plain text): 
  - ALLOWED_REDIRECT_ORIGIN = https://wahahockey.org
  - TOKEN_SCOPE = public_repo   # use 'repo' if your repo is private
- Configure routes (via Wrangler or Dashboard) so the worker runs at:
  - https://cms-oauth.wahahockey.org/auth
  - https://cms-oauth.wahahockey.org/callback

## 3) Configure Decap CMS (admin/config.yml)
```yaml
backend:
  name: github
  repo: Fp4Mail/wahahockey.org
  branch: main
  base_url: https://cms-oauth.wahahockey.org
  auth_endpoint: auth
```

## 4) Test
- Visit https://wahahockey.org/admin/
- Click “Login with GitHub”
- Approve OAuth for WAHA Hockey CMS
- You should land in the CMS with repo access per the chosen scope.

