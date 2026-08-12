# Sunrise

A private habit and sleep tracker that runs as an app on your phone.
Sleep log, daily checklist, a score out of 100, streaks and milestones.
All data stays on the device — nothing is uploaded anywhere.

---

## What goes in the repository

Put these **6 files in the root** of the repo — not inside a folder:

```
your-repo/
├── index.html            the whole app
├── manifest.json         name, icon and colours for the home screen
├── sw.js                 service worker, makes it work offline
├── icon-192.png          Android icon
├── icon-512.png          Android icon, large + maskable
├── apple-touch-icon.png  iPhone home screen icon
└── README.md             this file (optional)
```

Filenames must stay exactly as they are — `index.html` is what GitHub Pages
serves automatically, and the rest are referenced by name inside it.

---

## Step by step

### 1. Create the repository
1. Go to **github.com** and sign in
2. Click **+** (top right) → **New repository**
3. Repository name: `sunrise`
4. Select **Public** — required for free GitHub Pages
5. Do **not** tick "Add a README"
6. Click **Create repository**

### 2. Upload the files
1. On the empty repo page click **uploading an existing file**
2. Drag in all 6 files at once (the files themselves, not the folder)
3. Wait for all 6 to finish uploading
4. Click **Commit changes**

You should now see the 6 files listed in the repo.

### 3. Turn on GitHub Pages
1. Click **Settings** (top of the repo)
2. In the left sidebar click **Pages**
3. Under *Build and deployment* → *Source*, choose **Deploy from a branch**
4. Branch: **main** — folder: **/ (root)**
5. Click **Save**
6. Wait 1–2 minutes, then reload the page. Your link appears at the top:

```
https://YOURUSERNAME.github.io/sunrise/
```

A 404 for the first couple of minutes is normal — it is still building.

### 4. Add it to your home screen

**iPhone (must be Safari)**
1. Open the link in Safari
2. Tap the **Share** button (square with an arrow)
3. Scroll down → **Add to Home Screen**
4. Tap **Add**

**Android (Chrome)**
1. Open the link in Chrome
2. Tap **⋮** (top right)
3. Tap **Add to Home screen** / **Install app**
4. Tap **Install**

It now opens fullscreen with the sunrise icon and no browser bars.

---

## Updating it later

1. In the repo, click `index.html` → the pencil icon → paste the new version → **Commit changes**
   *(or use **Add file → Upload files** and drop the new `index.html` on top)*
2. Wait about a minute
3. Close the app completely and open it twice — the service worker serves the
   old cached copy once before picking up the new one

---

## Your data

- Stored only in the browser on the phone you use it on. It is never sent anywhere.
- Clearing browser data, or deleting the home screen icon on iOS, can erase it.
- iOS also clears site storage if a web app goes ~7 days without being opened.
- **Use the Backup tab.** "Save backup file" writes `sunrise-backup-DATE.json`
  to Files / your cloud drive. "Restore from a file" brings everything back.
  Do it weekly.
- A public repo means anyone with the URL can open the app. It does **not**
  expose your data — the repo only contains the app itself.
