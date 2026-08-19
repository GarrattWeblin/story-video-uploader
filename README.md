# Story Video Uploader — GitHub Pages site

The public site TikTok's reviewers will load. Contains the landing page,
Terms of Service, and Privacy Policy, plus the app icon.

## How to publish (one time, ~5 minutes)

### Option A — project repo with Pages enabled (recommended)

1. Create a **new public repository** on GitHub, e.g. `story-video-uploader`
   (do NOT add a README/license — keep it empty).
2. In the terminal on this machine, run:

   ```bash
   cd /home/garratt/tiktok-pipeline/tiktok-app-site
   git init
   git add .
   git commit -m "Story Video Uploader app site"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/story-video-uploader.git
   git push -u origin main
   ```

3. On GitHub: repo → **Settings → Pages** → Source: **Deploy from a branch** →
   branch `main`, folder `/ (root)` → Save.
4. Wait ~1 minute, then your site is live at:
   `https://YOUR_USERNAME.github.io/story-video-uploader/`

### Option B — user site (if you want it at the root domain)

1. Create a public repo named exactly **`YOUR_USERNAME.github.io`**.
2. Push the same files to it (`git remote add origin
   https://github.com/YOUR_USERNAME/YOUR_USERNAME.github.io.git`).
3. Site is live at `https://YOUR_USERNAME.github.io/` automatically.

## Then, in the TikTok developer portal

Set these URLs on your app (they're the ones TikTok's reviewers will open):

| Field | Value |
|---|---|
| **Website URL** | `https://YOUR_USERNAME.github.io/story-video-uploader/` (or `https://YOUR_USERNAME.github.io/`) |
| **Terms of Service URL** | `https://YOUR_USERNAME.github.io/story-video-uploader/tos.html` |
| **Privacy Policy URL** | `https://YOUR_USERNAME.github.io/story-video-uploader/privacy.html` |

And update the same values on the **Setup page** of your file server
(`http://192.168.8.111:8092/setup`) — it has copy buttons for each field.
