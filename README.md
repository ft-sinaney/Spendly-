# Spendly

Monthly salary and expense tracker. Data is stored on the device, saves automatically, and exports to Excel (one sheet per month plus a summary). It installs to the phone's home screen as an app.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app |
| `manifest.webmanifest` | App name, icon and colours used when installing |
| `sw.js` | Lets the installed app open without internet |
| `icons/` | Home-screen icons |
| `netlify.toml` | Netlify settings (publish folder, headers) |

## Deploy (GitHub → Netlify)

1. Push this folder to a new GitHub repository. The files must sit at the repo root, not inside a subfolder.
2. In Netlify: **Add new site → Import an existing project → GitHub**, then pick the repository.
3. Leave the build command empty. The publish directory is `.` (already set in `netlify.toml`).
4. Deploy. Every later `git push` redeploys automatically.

## Install on Android

1. Open the Netlify link in **Chrome**.
2. Tap **Install app** when it appears, or use **⋮ → Install app / Add to Home screen**. You can also use the **Install Spendly app** button under Profile.
3. Spendly opens from the home screen like a normal app.

To get an `.apk` file, paste the Netlify link into https://www.pwabuilder.com and choose **Android**.

## Updating the app

After changing `index.html`, change `VERSION` in `sw.js` (for example `spendly-v2`) so installed phones fetch the new version.

## Data safety

All records live in the browser storage of the phone. Uninstalling the app or clearing Chrome's site data erases them. Use **Export Excel** or **Download backup** from Profile regularly.
