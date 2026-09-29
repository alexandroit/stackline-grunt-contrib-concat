# Upstream review

Exact source: [grunt-contrib-concat@2.1.0](https://www.npmjs.com/package/grunt-contrib-concat/v/2.1.0), [75eaca2f9b7c5bb56ce1feb307f2a9106ba0b755](https://github.com/gruntjs/grunt-contrib-concat/commit/75eaca2f9b7c5bb56ce1feb307f2a9106ba0b755). Runtime task files match the integrity-checked upstream npm tarball byte-for-byte. Original authors and license are retained.

## Issue review (2026-09-29)

- [#181: Concatenating multiple source maps](https://github.com/gruntjs/grunt-contrib-concat/issues/181): Retain the synchronous source-map0.5 API and execute all upstream external/inline/CSS/JS map assertions.
- [#188: source-map0.7 incompatibility](https://github.com/gruntjs/grunt-contrib-concat/issues/188): Do not upgrade the runtime dependency to the incompatible asynchronous API.

No issue response or upstream contact was made. These are scoped compatibility decisions, not claims that every reported issue is fixed.

## Development maintenance

The original Grunt task fixtures and Nodeunit assertion bodies run unchanged. A small Node assert adapter preserves expected assertion counts and asynchronous done timeouts; it replaces obsolete Nodeunit/TAP dependencies. Obsolete JSHint and release-only grunt-contrib-internal tooling were removed. The current Grunt runner is development-only; package engines and runtime dependencies retain the upstream declarations. The same full fixture suite runs against an installed package archive.

Run `npm ci --ignore-scripts`, `npm test`, `npm run test:package`, and `npm audit --audit-level=low`. GitHub CI and CodeQL gate exact artifact publication with provenance and immutable release evidence.
