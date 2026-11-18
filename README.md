# Mark Databases

Versioned offline knowledge packs for the Mark Android assistant.

## Repository layout
- `catalog.json`: pack catalogue read by the Android app.
- `packs/`: downloadable JSON knowledge packs.

## Pack format
Each pack is UTF-8 JSON with:
- `id`: stable unique identifier.
- `name`: display name.
- `version`: integer version.
- `language`: BCP-47 language tag where possible.
- `description`: short description.
- `entries`: array of question/answer objects.

## Publishing rules
1. Keep pack IDs stable; increment version when contents change.
2. Validate JSON before committing.
3. Do not put private, copyrighted, or personal data into public packs.
4. Add a SHA-256 checksum to the catalogue before enabling verified downloads in the app.

The current catalogue is a starter. The Mark app does not yet download packs; downloader and checksum verification are planned.