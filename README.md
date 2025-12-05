# EXP BOOK

EXP BOOK is a small, privacy-first journaling web app designed to help you record mistakes,
acknowledge corrections, and build better habits over time. Everything runs entirely in the
browser — there are no accounts or servers, and your data is stored locally (in `localStorage`).

**This repository contains a simple single-page app and a landing page** you can open locally
in any modern browser.

**Key goals**:
- Provide a lightweight, distraction-free journaling experience.
- Keep all data local to the user's browser for privacy.
- Make it easy to export your data as JSON for backups.

**Features**
- Record daily entries (what went wrong / what to improve).
- Acknowledge entries to track when you've practiced a correction.
- Add short comments to entries.
- Search/filter entries client-side.
- Export data as JSON. (PDF export is not implemented in this simple build.)

**Repository files**
- `expbook.html`: Landing / marketing page. Click "Open EXP BOOK" to open the app.
- `app.html`: The journaling single-page app — add entries, acknowledge them, comment, and export JSON.
- `README.md`: This documentation.

Getting started (open locally)
- Open `expbook.html` in a desktop or mobile browser. From the page, click the "Open EXP BOOK" button.
- Or open `app.html` directly in the browser to jump straight into the journal UI.

Windows PowerShell example to open the landing page:
```powershell
Start-Process 'C:\Users\darsh\OneDrive\Desktop\websites\exp_book\expbook.html'
```

How the app stores data
- Entries and some metadata are stored in `localStorage` under the key `expData`.
- Acknowledgement tracking uses a small `lastAck` object stored in `localStorage`.
- Because data is local, clearing browser data, switching browsers, or using a different device
	will not carry over your journal unless you export and import the JSON.

Exporting and backup
- Use the "Export JSON" button in the app to download a `.json` file containing your entries.
- To back up, copy the downloaded JSON off-device (cloud storage, external drive, etc.).

Privacy and security notes
- No server: the app runs entirely in the browser and does not transmit data anywhere.
- If you want to protect the file on your device, use OS-level file encryption or a passworded archive.

Deployment ideas
- GitHub Pages: push this repository to GitHub and enable GitHub Pages to serve the static files.
	- If using GitHub Pages, set the repo's Pages source to the `master` branch (or `main`) and
		point the site to `/expbook.html` or `/` depending on your setup.
- Serve from any static hosting provider (Netlify, Vercel, Surge, etc.).

Troubleshooting
- If you still see an old password prompt after editing files, try a hard refresh or clear sessionStorage
	in the browser console: `sessionStorage.clear()` and reload the page.
- If data looks missing, check `localStorage` (`localStorage.getItem('expData')`) to inspect stored entries.

Contributing
- This is a small personal project — contributions are welcome. Open an issue or a PR with small,
	focused changes (bug fixes, responsive tweaks, or small features like PDF export).

Possible improvements
- Implement client-side PDF export (using `html2pdf` or `jsPDF`).
- Add import functionality to restore from an exported JSON backup.
- Add optional encryption for stored data (local passphrase-based encryption).

License
- This repository does not include a license file. Add a `LICENSE` if you want to specify reuse terms.

Enjoy using EXP BOOK — open `expbook.html` and start journaling.