# Changelog

## [0.2.0] - 2026-03-28

### Changed
- **Plugin frontend build format** — Changed from ES module + externals to IIFE format with window globals; ES module bare specifiers (`import 'react'`) don't work in browsers, IIFE with globals (`React`, `ReactDOM`, `ReactJSXRuntime`, `TanStackReactQuery`) resolves from host Panel's `window` exports
- **Template vite.config.ts** — Updated with `define: { 'process.env.NODE_ENV': 'production' }`, IIFE format, and complete globals mapping
- **Template index.ts** — Updated with window registry pattern (no ES exports)
- **Template package.json** — Updated dependency versions (React 19, Vite 8, TypeScript 5.9), added `@tanstack/react-query` as peer dependency

### Added
- CHANGELOG.md

## [0.1.0] - 2026-03-25

### Added
- Initial release of ACP Plugin SDK + CLI
- `acp-cli init` — Scaffold new plugin from template
- `acp-cli validate` — Validate manifest.json
- `acp-cli build` — Build plugin zip bundle (frontend + backend)
- `acp-cli publish` — Publish to ACP Market
- `acp-cli login` — Authenticate with Market
- Comprehensive documentation (9 guides)
