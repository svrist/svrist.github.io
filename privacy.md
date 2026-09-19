---
layout: default
title: Privacy Policy
permalink: /privacy
---

This Privacy Policy describes how **rclone** ("the app") handles information. The
app is a personal, self-hosted deployment of the open-source
[rclone](https://rclone.org/) tool, run by a single individual ("the operator")
on the operator's own private server. It also covers this website ("the site"),
which is a static, informational page about the app.

## Who operates the app

The app is operated by the operator for the operator's own personal use. It is
not offered as a public service and has no users or accounts other than the
operator's own. Questions can be sent to [s@vrist.dk](mailto:s@vrist.dk).

## Information the app accesses

The app connects to the **operator's own Google Drive account** using OAuth 2.0,
and only after the account holder has explicitly granted access. It is configured
to request the minimum access needed — Google Drive's `drive.file` scope — so it
can see and manage only the files it creates. Specifically, it accesses:

- the dedicated backup folder in the operator's Google Drive and the encrypted
  backup objects the app itself creates and manages there; and
- the basic Google account information required to authorize and maintain the
  connection.

The app does **not** access Gmail, Calendar, Contacts, Photos, or any other
Google service, and it does not access any Google Drive files that it did not
create.

## How the information is used

Information is used solely to:

- upload, verify, list, and delete the app's own backup objects in the operator's
  Google Drive; and
- download those objects to restore the operator's server.

The information is **not** used for advertising, profiling, or marketing, is
**not** sold, and is **not** shared with any third party. No human reads the
contents of the backups: the backup repository is encrypted on the operator's
server before it is uploaded, so Google Drive only ever holds encrypted data.

## How the information is stored and protected

- OAuth credentials (access/refresh tokens) are stored locally on the operator's
  own server, in rclone's configuration file, protected by filesystem
  permissions. They are sent only to Google to authorize requests.
- Backup data is encrypted by [restic](https://restic.net/) before upload, so the
  contents are not readable by the app, Google, or anyone else without the
  operator's backup password.

## Retention and deletion

Backup objects are retained according to the operator's retention policy
(currently seven daily and four weekly copies); objects that fall outside it are
deleted from Google Drive. The account holder can revoke the app's access at any
time at <https://myaccount.google.com/permissions>, which immediately ends the
app's ability to access Google Drive. Deleting the backup folder in Google Drive
removes the stored data.

## Google API Services — Limited Use

The app's use of information received from Google APIs will adhere to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## The website

The site does not collect, store, or process any personal information. It does
not use cookies, analytics, advertising, or any other tracking technology, and it
does not ask you to create an account or submit any data. The site is hosted by
GitHub Pages; as with any web host, GitHub may collect limited technical
information (such as IP addresses and request timestamps) in its server logs, as
described in the
[GitHub Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-privacy-statement).

## Children's privacy

The app and the site are not directed at children and do not knowingly collect
information from anyone.

## Changes to this policy

This policy may be updated from time to time. Any changes will be posted on this
page with an updated date below.

## Contact

If you have questions about this Privacy Policy, contact
[s@vrist.dk](mailto:s@vrist.dk).

_Last updated: 19 September 2026_
