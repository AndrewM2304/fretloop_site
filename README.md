# Fretloop Site

This folder is a static website for Fretloop.

## Files

- `index.html`: minimal homepage with the app icon, app name, and App Store link
- `privacy/index.html`: public privacy policy page
- `app-map/`: Flutter web build of the flutter-map visualiser with the
  Fretloop `.appmap` embedded as its default bundle
- `icon.svg`: shared icon used by both pages

The app map contains fictional seeded data only. It is intentionally marked
`noindex` but remains publicly accessible to anyone with the URL when deployed
on GitHub Pages. The upstream flutter-map project does not currently publish a
licence, so obtain the author's permission before distributing its compiled
visualiser publicly.

## Before You Publish

Update the App Store link in `index.html`:

- replace `https://apps.apple.com/` with the real App Store URL once the app is live

The privacy policy already includes a fixed effective date in the footer.

## Recommended GitHub Pages Setup

The cleanest option is to publish this folder from the root of a dedicated GitHub Pages repository or a dedicated Pages branch.

### Option 1: Dedicated repository

1. Create a new GitHub repository for the public site.
2. Copy the contents of `fretloop-privacy-site/` to the repository root.
3. In the repository settings, open `Pages`.
4. Under `Build and deployment`, choose `Deploy from a branch`.
5. Select the branch that contains these files.
6. Select the repository root as the publishing folder.

This gives you a stable public site and keeps it separate from the app repo.

### Option 2: Dedicated branch

1. Create a branch just for the public site.
2. Put `index.html` at the branch root.
3. Keep `privacy/index.html` and `icon.svg` in the same branch.
4. In the repository settings, open `Pages`.
5. Choose the branch and publish from the root folder.

This is useful if you want the site inside the app repository but still published separately.

### Option 3: Publish from the app repository

If you want to host the site from this repo, copy the files into a Pages-supported location such as `/docs`, then publish that folder from GitHub Pages.

## Expected URLs

If this site is published from a repository root:

- Home: `https://<owner>.github.io/<repo>/`
- Privacy: `https://<owner>.github.io/<repo>/privacy/`
- App map: `https://<owner>.github.io/<repo>/app-map/`

If it is published from a dedicated `.<github>.io` repository, the URLs will be rooted at the domain itself.

## Adding a Custom Domain Later

When you buy a domain:

1. Add a `CNAME` file at the site root.
2. Put the domain name in that file.
3. Set the custom domain in GitHub Pages settings.
4. Wait for DNS and Pages to finish provisioning.

## When To Update The Privacy Policy

Update the privacy policy before shipping a new app version if Fretloop adds:

- user accounts
- cloud sync
- analytics
- crash reporting
- email capture
- support chat
- external APIs beyond Apple services
- advertising
- data sharing with third parties
