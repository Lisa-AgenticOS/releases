# LisaOS Releases

This public repository is the binary distribution origin for LisaOS system and
application updates. LisaOS clients access these files through
`https://updates.lisaos.dev`; immutable payload storage is provided by GitHub
Releases.

The repository contains only compiled release artifacts, signed public
metadata, checksums, SBOM/provenance records, and the small channel pointers in
`channels/`. LisaOS source code and private signing keys do not belong here.

Release families are independent:

- `os-<channel>-<release>-<architecture>-desktop` for Desktop system updates;
- `os-<channel>-<release>-<architecture>-server` for Server system updates;
- `apps-<channel>-<release>-<architecture>` for application-set updates.

Existing release tags and assets are immutable. A channel pointer advances
only after every planned asset has been uploaded and verified. The signed OS
metadata and signed app manifest remain the authority for all downloaded
bytes; the pointer and CDN are untrusted transport indexes.

Project source and development issues live in the repositories under the
[Lisa-AgenticOS organization](https://github.com/Lisa-AgenticOS).
