# Security and data-flow overview

This is a source-informed overview of the prepared customer app, dated October 26, 2026. It is not a complete runtime traffic analysis or independent security audit.

- LyricFlow reads available song metadata, playback position/state and artwork from the selected player or macOS Now Playing. Available playback controls are sent back to that player.
- Music/Spotify Automation permission may be needed for direct control. Users should grant it only for players they intend to use; support varies by client and OS.
- Lyrics matching and retrieval can send recording identifiers or song/artist/album/duration metadata to the configured lyrics service and providers. Spicy Lyrics is the primary source, with LRCLIB fallback. Artwork/catalog lookups can contact additional services. “No data leaves the Mac” would be inaccurate.
- Preferences are local. Optional account/provider credentials use macOS Keychain. This does not establish that all app data is encrypted or that no other process can ever access it.
- Customer packages exclude owner-only entitlements and payment Test Mode configuration. Merchant API and signing secrets belong on the service, not in distributed app files.
- The prepared Pro flow uses hosted checkout and signed access responses. Payment/customer data is handled by the relevant providers. One live owner purchase, verified Pro unlock and relaunch persistence are confirmed in build191. Recovery email delivery and explicit confirmation in the initiating app succeeded October27. Clean second-Mac recovery and live refund/revocation remain unverified.
- The reviewed direct-distribution entitlement is Apple Events Automation. A minimal entitlement list alone is not a security guarantee.

See the official [privacy notice](https://lyricflow.studio/privacy/) for user-facing disclosures. Report a concern through the [official support contact](https://lyricflow.studio/refunds/); avoid publishing credentials or payment proofs in GitHub issues.
