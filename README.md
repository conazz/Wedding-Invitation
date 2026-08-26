# Charles & Justine — Wedding Invitation Site

Static, self-contained wedding invitation. Each seat-count version lives in its own folder so it gets a clean URL once published with GitHub Pages.

## Structure

```
/            landing page — links to all 7 versions
/1/          1 seat version   → yoursite.com/1/
/2/          2 seat version   → yoursite.com/2/
/3/          3 seat version   → yoursite.com/3/
/4/          4 seat version   → yoursite.com/4/
/5/          5 seat version   → yoursite.com/5/
/6/          6 seat version   → yoursite.com/6/
/7/          7 seat version   → yoursite.com/7/
```

Every page is a single self-contained `index.html` (fonts load from Google Fonts; all photos and the RSVP QR code are embedded directly in the file, so nothing else needs to be uploaded).

## 1. Push these files to GitHub

**Option A — Upload through the GitHub website (no command line needed)**
1. Go to your repo: https://github.com/conazz/Wedding-Invitation
2. Click **Add file → Upload files**.
3. Drag in the `index.html` at the top level, plus the `1/`, `2/`, `3/`, `4/`, `5/`, `6/`, `7/` folders (drag the whole folders in — GitHub keeps the folder structure).
4. Scroll down and click **Commit changes**.

**Option B — Push with git** (if you have git installed and are comfortable with the terminal)
```bash
git clone https://github.com/conazz/Wedding-Invitation.git
cd Wedding-Invitation
# copy index.html and the 1/ ... 7/ folders from this delivered package into this folder
git add .
git commit -m "Add wedding invitation site"
git push
```

## 2. Turn on GitHub Pages

1. In the repo, go to **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Under **Branch**, choose `main` (or `master`) and folder `/ (root)`, then **Save**.
4. GitHub will publish the site within a minute or two at:
   `https://conazz.github.io/Wedding-Invitation/`

Your guest links will then be:
- `https://conazz.github.io/Wedding-Invitation/1/`
- `https://conazz.github.io/Wedding-Invitation/2/`
- ... through `/7/`

And the landing page (all versions) at the root URL itself.

## 3. Optional — custom domain

If you own a domain (e.g. `charlesandjustine.com`), add it under **Settings → Pages → Custom domain**, and add the DNS records GitHub shows you at your domain registrar. Pages will then serve at your own domain instead of the `github.io` address.

## Updating content later

If you ever need to change wording, photos, or the theme, edit the corresponding `index.html` file(s) and re-upload/push — GitHub Pages redeploys automatically within a minute or two of any push to the published branch.
