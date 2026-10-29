# Signing, installation and checksums

The current public build is ad-hoc signed and **not notarized by Apple**. Apple has not verified its developer identity. Signature integrity checks do not mean Apple security approval. Some managed Macs may refuse it.

No installer is hosted in this repository. Use the official website, and match its version and SHA-256 with the corresponding dated report. Private-candidate checksums must not be treated as identifiers for a later release.

When opening an official download, make any per-app trust decision yourself using [Apple's guidance](https://support.apple.com/102445). Do not disable Gatekeeper or remove quarantine through a script. Stop and contact support if macOS reports malware or a damaged application.

Updates are manual. Quit the old LyricFlow copy before replacing or opening a new one; keep one active copy. A changed ad-hoc-signed build may cause another Keychain permission prompt.

A SHA-256 match establishes that two files contain the same bytes. It does not establish that the program is safe, independently audited, notarized or compatible with every Mac.
