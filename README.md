# RBI–NBFC Regulation Map

An interactive map of the Reserve Bank of India Acts, Master Directions, schemes and notifications that apply to non-banking financial companies (NBFCs), including housing finance companies. For each instrument it shows the key concepts, obligations, timelines, consequences of breach, who it applies to under Scale Based Regulation, and how it connects to other instruments.

**Live site:** https://sayakchandra-lawyer.github.io/rbi-nbfc-regulation-map/

## Not legal advice

This is an independent, unofficial summary prepared for general information. It may be incomplete or out of date and is not endorsed by the Reserve Bank of India. Verify every point against the official text on [rbi.org.in](https://www.rbi.org.in) and the Gazette before relying on it. Entries marked with an amber "!" contain items that have not yet been checked against the primary text.

## How the site is organised

```
index.html                         the app (D3, no build step)
maps/manifest.json                 list of maps and their settings
maps/rbi-nbfc/rbi_nbfc_register.json   instruments: obligations, timelines, consequences, sources
maps/rbi-nbfc/rbi_nbfc_graph.json      nodes and links between instruments and NBFC categories
maps/rbi-nbfc/updates.json             RBI items from the last 7 days, with a general impact view
maps/rbi-nbfc/glossary.json            plain-language definitions of key terms
```

The page reads `maps/manifest.json` and then the register and graph files it names. Code and data are separate:

- **Weekly data refresh:** replace the JSON files in `maps/rbi-nbfc/` and commit. Keep `meta.as_of` the same in both files; the page warns when they differ.
- **New sector map:** add a folder under `maps/` and an entry in `manifest.json`. A map switcher appears once there is more than one map.

Register as of the date shown in the page header.
