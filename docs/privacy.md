---
title: kaikuja-publish – Privacy Policy
---

# Privacy Policy — kaikuja-publish

*Last updated: 30 October 2026*

**kaikuja-publish** is an open-source command-line tool written and used by Tuukka Pitkänen,
the host of the podcast *Kaikuja Kaikkeudesta*, to publish the podcast's episodes and clips
to his own YouTube channel and other channels. It runs only on his own computer. It has no
server, no website login, no analytics and no other users.

## YouTube API Services

kaikuja-publish uses **YouTube API Services**. By using it you agree to be bound by the
[YouTube Terms of Service](https://www.youtube.com/t/terms). YouTube data is handled by
Google under the [Google Privacy Policy](https://policies.google.com/privacy)
(<http://www.google.com/policies/privacy>).

## What information is accessed

When the channel owner signs in with Google (OAuth 2.0), the tool receives an access token
and a refresh token for the scope `https://www.googleapis.com/auth/youtube`. With them it:

- uploads videos that the owner has produced (`videos.insert`), always as *private* first;
- sets their title, description, tags, category, language and thumbnail (`videos.update`,
  `thumbnails.set`), and makes them public on the owner's command;
- reads the owner's own channel ID, uploads playlist and the titles, IDs and privacy status
  of the five most recent uploads (`channels.list`, `playlistItems.list`).

It does not access any other YouTube user's data, comments, subscribers, analytics or
viewing history.

## How information is stored and used

- OAuth tokens are stored only on the owner's computer, in
  `~/.config/kaikuja-publish/tokens.json`, readable only by the owner (file mode 600).
- Video IDs and URLs returned by YouTube are written into the owner's own episode text
  file, so the tool knows which steps are already done.
- Nothing is sent anywhere except to the APIs of the services the owner publishes to
  (YouTube, Podbean, WordPress, Mastodon, Bluesky, LinkedIn, Meta). No data is sold,
  shared with third parties, or used for advertising.
- The tool does not use cookies or any tracking.

## Revoking access and deleting data

- Access can be revoked at any time on the Google security settings page:
  <https://security.google.com/settings/security/permissions>
  (also at <https://myaccount.google.com/permissions>).
- Deleting `~/.config/kaikuja-publish/tokens.json` removes all stored tokens; no copy exists
  anywhere else. After access is revoked the stored tokens no longer work and the file is
  deleted. Apart from the video IDs and URLs mentioned above, no YouTube API data is stored.

## Contact

Tuukka Pitkänen — questions and requests via
[GitHub issues](https://github.com/pitkanentuukka/kaikuja-publish/issues)

[Terms of use](terms.html) · [Project home](https://github.com/pitkanentuukka/kaikuja-publish)
