# Household Ledger

Our private dashboard for property, rent, tenants, budget, investments and key dates.

- **Page:** `index.html`, published free by GitHub Pages.
- **Logins and data:** Google Firebase (free Spark plan): Authentication for the two logins, Cloud Firestore for the data.
- **Security:** only the email addresses listed in `firestore.rules` can read or change anything. This folder holds no financial data, only the page code.

## Everyday use
- Sign in with your email and password. "Forgot password?" on the login screen sends a reset link.
- **Settings → Download backup** once a month. Keep the file somewhere safe.
- **Key dates → Add to my calendar** puts every renewal into your phone calendar with alerts. Press it again after adding new dates.

## Managing logins
Firebase console → your project → **Authentication → Users**.
- Add a person: **Add user**, then add their email to `firestore.rules` and publish the rules (Firestore Database → Rules → Publish).
- Remove a person: delete the user, and remove their email from the rules.

## Changing the page
Ask Claude: "Update my Household Ledger in the GitHub repo <owner>/<repo>: …". Claude edits `index.html` and pushes; GitHub Pages republishes in a minute or two. Your data is not touched by page changes.

## Files
| File | What it is |
|---|---|
| `index.html` | The whole app |
| `config.js` | Which Firebase project to use (not a password) |
| `firestore.rules` | Copy of the security rules pasted into Firebase |
| `robots.txt` | Asks search engines not to list the site |
