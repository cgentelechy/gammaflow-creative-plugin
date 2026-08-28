# GammaFlow Creative Plugin

This is the thin, distributable Codex plugin for GammaFlow's private creative-reference service.

It supports two authorized workflows:

- **Ad slate:** generate exactly 12 ad concepts from one campaign input and one expiring reference packet.
- **Cold-email slate:** generate three distinct three-email sequences from one campaign input and one expiring reference packet.

Generation runs in the signed-in Codex account. The private gateway returns a single sanitized packet and does not expose source names, database IDs, source images, original copy, lineage, or general database-search tools.

## Installation

Add this repository as a Codex plugin marketplace:

```text
/plugin marketplace add https://github.com/cgentelechy/gammaflow-creative-plugin
```

Then install `creative-library-remote` from the `gammaflow-creative` marketplace. The first authorized workflow will open the GammaFlow sign-in flow for a manually issued invitation.

The remote gateway must be live and registered with Codex before installation is useful.

## Repository boundary

This repository intentionally contains only the public plugin package. The private gateway, Supabase schema, master skills, source library, and credentials live elsewhere.
