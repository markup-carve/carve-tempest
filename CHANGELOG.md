# Changelog

All notable changes to Carve for Tempest are documented in this file.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and the project follows [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.1.1] - 2026-10-08
### Changed

- Require carve-php `^0.1.11`, up from `^0.1.9`. That release added the
  `destination-denied` render-loss code, so a denied destination such as
  `[x](javascript:alert(1))` now appears in `RenderReport::$losses` and
  `renderWithReport(..., strictLosses: true)` rejects the document instead of
  rendering it with a blanked target. On 0.1.9 the same document reported
  nothing and strict mode accepted it.

## [0.1.0] - 2026-09-20

### Added

- First release: Carve rendering for Tempest applications
- Safe-by-default `x-carve` Tempest View component
- Discoverable singleton `CarveRenderer` service
- Tempest-native configuration with named profiles and extension registration
- Optional content-hash rendering cache through Tempest Cache
- Rendering diagnostics, profile violations, and bounded loss reports
- Opt-in source-line annotations for editor preview synchronization
- HTML, Markdown, plain-text, and ANSI service outputs
- Container-resolved include resolvers with structured results and bounded expansion
- Dependency-aware include caching through resolver-provided invalidation keys
- Named renderer configurations and per-call profile overrides
- Reusable PHPUnit assertions for rendering, safety, and warnings
