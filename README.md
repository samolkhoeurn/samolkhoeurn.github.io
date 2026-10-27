# samol.me

Personal site, hosted on GitHub Pages from this repository (`samolkhoeurn.github.io`) with the custom domain **samol.me**.

| Path | What |
|---|---|
| `/` | redirects to `/home/` |
| `/home/` | lock-screen style landing page: live clock, rotating quotes (English + Khmer), tiles to the other sections |
| `/wedding/` | wedding countdown to 3 January 2027 with photo slideshow, petals and gallery — edit the `CONFIG` block at the bottom of `wedding/index.html` (names, venue, photo list) |
| `/wedding/?i=<code>` | personal invitation: Khmer invitation card with the guest's name + RSVP (join / not, head count, who). Replies are stored in Firestore `rsvps/{code}`; guests live in `guests/{code}` |
| `/wedding/admin/` | private guest list (same admin login as the quiz): add guests, copy their personal links / invitation message, see replies and totals, download CSV |
| `/career/` | CV page (print-friendly) — the PDF lives at `assets/Samol-Khoeurn-CV.pdf` |
| `/quiz/` | served from the separate `quiz` repository (GitHub project site) |
| `assets/photos/` | photos used by home and wedding (`home.jpg`, `wedding-NN.jpg`, resized to ≤ 2000 px) |

No build step: plain HTML/CSS/JS, Google Fonts only. The wedding RSVP reuses the quiz site's Firebase project: it imports `/quiz/firebase-config.js` (served by the `quiz` repo under the same domain) and needs the `guests`/`rsvps` section of that repo's `firestore.rules` published.
