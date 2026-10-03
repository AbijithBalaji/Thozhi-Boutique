# Thozhi-Boutique

Simple landing page for **Thozhi boutique** ready to publish with GitHub Pages.

## Publish on GitHub Pages

1. Push this repository to GitHub.
2. Go to **Repository → Settings → Pages**.
3. Under **Build and deployment**, choose:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` (or your default branch), folder `/ (root)`
4. Click **Save**.
5. Wait a minute and open the generated Pages URL (usually `https://<username>.github.io/<repo>/`).

## Connect your GoDaddy domain

### 1) Add custom domain in GitHub

1. In **Settings → Pages**, enter your domain in **Custom domain** (for example `thozhiboutique.com` or `www.thozhiboutique.com`).
2. Click **Save** and enable **Enforce HTTPS** after DNS is correctly configured.

### 2) Configure DNS in GoDaddy

If you want **root domain** (`thozhiboutique.com`):
- Add these `A` records for `@`:
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`

If you want **www subdomain** (`www.thozhiboutique.com`):
- Add a `CNAME` record:
  - Host: `www`
  - Points to: `<username>.github.io`

Recommended:
- Keep both working by setting `www` as `CNAME` to `<username>.github.io`, then set GitHub Pages custom domain to your preferred primary domain.

### 3) Wait for DNS propagation

- DNS updates can take a few minutes to 24–48 hours.
- Once propagated, refresh GitHub Pages settings and verify HTTPS is enabled.