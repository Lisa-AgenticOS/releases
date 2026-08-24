# LisaOS Releases

This public repository is the complete transport origin for LisaOS system and
application updates. GitHub Pages serves the small signed channel metadata at
`https://updates.lisaos.dev/v1/`; immutable payload storage is provided by
GitHub Releases in this repository.

The repository contains only compiled release artifacts, signed public
metadata, checksums, SBOM/provenance records, and the Pages channel trees under
`v1/`. LisaOS source code and private signing keys do not belong here.

Release families are independent:

- `os-<channel>-<release>-<architecture>-desktop` for Desktop system updates;
- `os-<channel>-<release>-<architecture>-server` for Server system updates;
- `apps-<channel>-<release>-<architecture>` for application-set updates.

Existing release tags and assets are immutable. A channel advances only after
every planned release asset has been uploaded and verified; one final commit
then atomically replaces the selected lineage's signed metadata under
`v1/<channel>/<architecture>/<edition>/`. The Pages branch and GitHub's asset
CDN are untrusted transport. Threshold-signed OS metadata and detached-signed
app manifests authenticate all bytes on the device before staging or
activation.

Large OS images, partitions, UKIs, and app archives must never be committed to
the Pages branch. Release tooling and source live in the private LisaOS source
repositories; this public origin accepts only compiled artifacts and public
verification material.

Project source and development issues live in the repositories under the
[Lisa-AgenticOS organization](https://github.com/Lisa-AgenticOS).
