# Recovery and Wellness Massage — Custom Website

Static HTML/CSS/JS site prepared for GitHub + Vercel. No build tooling is required.

## Pages
- `index.html`: cinematic YouTube hero, services, About, GHL offer popup.
- `services.html`: service pricing and treatment descriptions.
- `about.html`: Cadence biography and supplied portrait.
- `book.html`: embedded GHL appointment request form, with personal follow-up messaging.

## Deployment
1. Create a new GitHub repository and upload all files and the `assets` directory to the repository root.
2. Import the repository into Vercel and choose **Other** / no framework; root directory `./`.
3. Deploy. If needed, set Framework Preset to `Other` and leave Build Command empty.
4. Verify `/`, `/services.html`, `/about.html`, `/book.html`, popup, video and appointment request form.
5. Connect the custom domain in Vercel and update DNS only when ready to go live.

## Important notes before launch
- The six technique photos are referenced from the existing website's LeadConnector CDN, because they could not be downloaded during the build. They may stop working if the old GHL assets are removed. Replace them with local licensed images in `assets/` and update the corresponding `src` attributes in `services.html` and the background image URL in `styles.css` before retiring those assets.
- The YouTube hero uses `youtube-nocookie.com`; autoplay may be blocked by certain browsers and YouTube may show overlays/branding. Use a hosted MP4 if strict visual control is needed.
- The supplied GHL form is configured with `alwaysShow`, so it may open whenever the homepage loads; change trigger settings in GHL if it is too intrusive. Confirm any offer conditions and that consent text/privacy handling are appropriate before launch.
- Appointment requests use the supplied GHL form ID `OkX8swKVKHtRoyFsrIaW`. Test submissions, notifications, form consent settings, and your GHL follow-up workflow before launch.
- Business email, street address, published hours and social links were not independently verified, so they are intentionally excluded.
- Keep the existing DNS live until a Vercel preview is approved.
- The site footer includes exactly the requested credit text **Created by Wayfinder Media**, linking to https://wayfindercreative.net/ and displaying the uploaded Wayfinder Creative logo.

## Updating content
- Service prices: edit `services.html` and matching featured prices in `index.html`.
- Business copy: edit the corresponding `.html` page.
- Colors/layout: edit `styles.css`.
- Hero YouTube video: change the `4_M67m4HPCk` identifier in `index.html` (including `playlist=`).
- GHL popup or appointment-request form: update embed URLs in `index.html` or `book.html`.

## Local preview
Use a static HTTP server from this directory, such as `python -m http.server 8000`, then browse to http://localhost:8000/.

## October 2026 appointment request update
- Replaced the booking calendar with GHL form `OkX8swKVKHtRoyFsrIaW`.
- Updated navigation and booking calls-to-action across all four pages.
- Appointment requests are **not** confirmed bookings. Set up Cadence's follow-up notifications inside GoHighLevel separately.
- Original image assets are **not** included in this update because they were not among the files supplied. Keep the existing `assets/` folder in your GitHub repository unchanged when uploading these files.

## Latest edit
The booking page now contains just the centered appointment-request GHL form; the introductory side section was removed.
