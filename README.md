# SNEWSE documentation

This repository contains the SNEWSE documentation site built with Mintlify.
Published pages are MDX; `docs.json` owns navigation and site configuration.

## Local preview

With the Mintlify CLI installed, run from this repository root:

```powershell
mint dev
```

The default preview is `http://localhost:3000`. A different available port can be
selected with `mint dev --port 3001`.

## Documentation changes

[AGENTS.md](AGENTS.md) contains documentation scope, authority, writing, and
verification guidance. The installed Mintlify skill is under `.agents/skills/`.

From the repository root:

```powershell
mint validate
mint broken-links
```

Imported originals in `to-mintlify/` and local migration notes under
`.agents/project/` remain in the working folder. Both are excluded from Git and
Mintlify so the published repository has one documentation authority.

Publishing uses the repository connection configured in the Mintlify dashboard.
The connected branch and deployment result should be checked when publishing.
