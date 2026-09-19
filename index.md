---
layout: page
title: rclone
---

**rclone** is the name of this application ("the app"). It is a personal,
self-hosted deployment of the open-source [rclone](https://rclone.org/) tool,
operated for a single individual's own accounts. It is not a public service: it
has no sign-up, no user accounts, and no third-party users.

## Purpose

The app performs scheduled, encrypted off-site backups of a private home-lab
server. Using rclone's Google Drive backend, it uploads a
[restic](https://restic.net/) backup repository — a SQLite database, a FIT-file
mirror, and configuration belonging to a personal training service — into a
dedicated folder in the operator's **own** Google Drive. It can also download
those objects again to restore the server.

The only thing it writes to Google Drive is the encrypted backup repository it
creates. It does not read, collect, or process data belonging to anyone else, and
it is not used for anything other than backing up and restoring the operator's
own files.

## Google account access

rclone connects to Google Drive with OAuth 2.0 using access that the account
holder explicitly grants. The app requests only the Google Drive access it needs
to store and manage its own backup files. Access can be revoked at any time at
<https://myaccount.google.com/permissions>. See the
[Privacy Policy](/privacy) for what is accessed and how it is handled.

## Links

- [Privacy Policy](/privacy)
- [Terms of Service](/tos)

## Contact

[s@vrist.dk](mailto:s@vrist.dk)
