# 2A School Manager website

The marketing and download page for 2A School Manager, built in the same layout as the 2A FlowBooks site
(https://2aflowbooks.github.io/) in School Manager's navy and gold. One page, no build step.

## Files

- `index.html`: the whole page (styles and scripts inside it)
- `img/`: screenshots of the real app with made-up test students (WebP)
- `favicon.ico`, `favicon-32.png`, `apple-touch-icon.png`, `icon-192.png`: logo A icons

## Publishing (same address style as 2A FlowBooks, but as an organisation)

1. Signed in as kingzizou, go to github.com/organizations/plan and create a **free organisation** called **2aschoolmanager**
   (no second login needed; you are its owner).
2. In it, create a **public** repository named exactly **2aschoolmanager.github.io**.
3. Either upload everything in this folder (keep the `img` folder) with **Add file > Upload files**, then Commit,
   or give the Claude GitHub app access to the organisation (github.com/apps/claude/installations/select_target)
   so a Claude session can push the files for you.
4. After a minute or two the site is live at **https://2aschoolmanager.github.io/**
   (Settings > Pages should show "Deploy from a branch: main / root"; set it if not).

When the page changes, upload only the changed files again.

## Things to edit

Everything a shop owner would change is in the `CONFIG` block near the bottom of `index.html`:

- `pricing`: price per user a month, user-count discounts, period discounts, longest licence, most users.
  Set `perUserMonth: null` to hide the figures and show "Ask us" instead.
- `downloads`: the file names attached to every release in kingzizou/2A-School-Manager-releases
  (the fixed-name copies, so the links always give the newest version).
- `bank`, `whatsapp`, `email`: how schools pay and reach you.
- `termsUrl`, `privacyUrl`, `refundUrl`: add these pages for School Manager, then put their file names here
  and the footer shows the links.
- `flowbooksUrl`: where the "Also from 2A" section sends people.

The "New in 1.0.7" bar at the top and the feature cards are plain HTML; update them with each release.
