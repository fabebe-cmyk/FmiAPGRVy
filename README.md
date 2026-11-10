# AI for Grocery — One Grocery, Two Ways In (FMI APGR 2027)

An educational, industry-wide static landing page (no build step) about how AI can improve grocery performance across operations, asset protection, safety, risk management, cybersecurity, privacy and food safety, for FMI APGR 2027, April 12–15, 2027,
Westin Dallas Central Park, Dallas, Texas. Upload this whole folder as-is.

## What's in the folder

- `index.html` — the landing page
- `get-resource.html` — the lead-magnet form page (`get-resource.html?r=<slug>`)
- `resources.js` — the FMI resources used as lead magnets (title, description, cover, FMI link)
- `styles.css` — i3 brand styling (brand kit rev. 20260214: Helvetica Neue + Barlow; #00588F, #002447, #DF1E71, #00A661, #FFC107)
- `assets/` — grocer logos (from the FMI APGR page), FMI resource covers and conference photos
- `.nojekyll` — tells GitHub Pages to serve the files exactly as they are

GSAP, ScrollTrigger and anime.js load from cdnjs; Barlow loads from Google Fonts.

## Deploy with GitHub Pages

1. Create a new repository on GitHub (for example `i3-apgr-2027`).
2. From this folder:

```bash
git init
git add .
git commit -m "Add i3 landing page for FMI APGR 2027"
git branch -M main
git remote add origin https://github.com/<your-username>/i3-apgr-2027.git
git push -u origin main
```

3. In the repo, open **Settings → Pages**, set **Source** to **Deploy from a branch**, choose **main** and **/ (root)**, then **Save**.
4. After about a minute the page is live at `https://<your-username>.github.io/i3-apgr-2027/`.

## Before it goes live

1. **Forms.** Both forms are prototypes and send nothing. Set `FORM_ENDPOINT` (near the top of the script in
   `index.html` and `get-resource.html`) to the URL that should receive the JSON POST (CRM / marketing automation).
2. **Dates.** The page says April 12–15, 2027. The solution-provider video asks about "April 12th–14th" in its
   on-screen question; re-export it if the dates must match.
3. **Permissions.** Confirm clearance for: Doug Baker's and Parker Griebel's photos and quotes; Scott Ziter's quote; the
   grocer logos (copied from the FMI APGR page); and the FMI resource covers and statistics.
4. **Fonts.** Helvetica Neue is used where installed (Windows falls back to Arial). Add licensed web-font files and an
   `@font-face` rule in `styles.css` to make it identical everywhere.
5. **Routing.** "Connect with an FMI Committee Member" and the forms route to i3 (info@i3international.com) for now.
   Point them to FMI once a committee contact is named.
6. **Footer.** States that i3 developed the page as an FMI member and that it is not an official FMI publication.

## Run locally

```bash
python -m http.server 8767
```

Open http://localhost:8767/
