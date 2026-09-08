---
title: Versio Privacy Policy
layout: default
---

# Versio — Privacy Policy

_Last updated: 2026-09-08_

Versio ("the plugin", "we", "the developer") is a Figma plugin that snapshots your design tokens, variables, and styles, computes differences between versions, and suggests a semantic version bump. This policy explains what data the plugin touches, where it goes, and who can see it.

## Data the plugin reads

To build a snapshot, Versio reads the following from the Figma file you run it on: variable names, values, and types (colors, numbers, strings, booleans); variable collections and modes; paint/text/effect/grid style definitions; and the internal Figma IDs used to detect renames vs. genuine additions or removals. This is design-system data — colors, spacing, typography, and so on — not personal information about you or your team, beyond whatever names you've given your own tokens and styles.

## Where that data is stored

Every snapshot Versio creates is stored using Figma's own document plugin data API, directly inside the Figma file itself. It stays wherever your Figma file already lives and is subject to Figma's own storage, sync, and access controls. The developer of Versio has no server, and never receives, stores, or has access to your design token data.

One setting — your naming-convention preference — is stored locally on your device via `figma.clientStorage`, which is per-user, per-plugin storage provided by Figma. It never leaves your machine through any action of the plugin's.

## Optional: GitHub Gist backup

Versio can optionally push a copy of your latest snapshot to a GitHub Gist you control. This feature is off unless you turn it on. To use it, you enter a GitHub personal access token and a Gist ID into the plugin's Gist settings panel.

- Your token and Gist ID are stored locally via `figma.clientStorage` — the same per-user, local storage described above. They are never transmitted to, or stored by, the developer of Versio.
- When you take a snapshot with Gist backup configured, the plugin makes one network request, directly from your Figma client to GitHub's own API (`api.github.com`), to update your Gist with the current snapshot JSON. This is the only network destination Versio ever contacts, and it's declared in the plugin's manifest.
- You can change or clear your token and Gist ID at any time from the Gist settings panel. Revoking the token on GitHub's side (Settings → Developer settings → Personal access tokens) immediately stops the plugin from being able to use it.
- Anyone with access to that Gist — including anyone you've shared its link with, or the public, if you created it as a public Gist — can see the snapshot JSON pushed to it. Versio doesn't control Gist visibility; that's a setting on the Gist itself, which you create and own.

## Third parties

The only third party Versio ever communicates with is GitHub, and only when you've opted into Gist backup, for the single request described above. Versio does not use analytics, crash reporting, advertising, or any other third-party service. It doesn't sell, rent, or share your data with anyone, because it doesn't collect or hold your data in the first place.

## Children's privacy

Versio is a professional design tool distributed through Figma's Community and isn't directed at children. It doesn't knowingly collect information from anyone under the age required to hold a Figma account.

## Changes to this policy

If this policy changes, the updated version will be posted at this same location with a new "Last updated" date.

## Contact

Questions about this policy or how Versio handles data can be sent to versio.plugin@hotmail.com.

---

[Terms & Conditions](./terms.html)
