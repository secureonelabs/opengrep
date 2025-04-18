# Changelog

## [1.1.5](https://github.com/opengrep/opengrep/releases/tag/v1.1.5) - 18-04-2025

### Improvements

* Performance improvements by @maciejpirog and @dimitris-m in #221
* Add workflows for Intel Mac by @dimitris-m in #219

### Bug fixes

* Ensure that `min-version:` in rules is respected by @dimitris-m in #220

**Full Changelog**: https://github.com/opengrep/opengrep/compare/v1.1.4...v1.1.5


## [1.1.4](https://github.com/opengrep/opengrep/releases/tag/v1.1.4) - 14-04-2025

### Improvements

* PHP: Add arrow functions to the menhir parser by @maciejpirog in #205

### Bug fixes

* Fix logging mutex by @dimitris-m and @maciejpirog in #208

**Full Changelog**: https://github.com/opengrep/opengrep/compare/v1.1.3...v1.1.4


## [1.1.3](https://github.com/opengrep/opengrep/releases/tag/v1.1.3) - 10-04-2025

### Improvements

* Fix string templates in Kotlin by @maciejpirog in #191
* Add union types to PHP menhir parser by @maciejpirog in #201

### Bug fixes

* Fix: .semgrepignore not working on windows when path is not relative by @dimitris-m in #194

**Full Changelog**: https://github.com/opengrep/opengrep/compare/v1.1.2...v1.1.3


## [1.1.2](https://github.com/opengrep/opengrep/releases/tag/v1.1.2) - 02-04-2025

### Improvements

* Fix string literals in parser for C# by @maciejpirog in #186

**Full Changelog**: https://github.com/opengrep/opengrep/compare/v1.1.1...v1.1.2


## [1.1.1](https://github.com/opengrep/opengrep/releases/tag/v1.1.1) - 31-03-2025

### Bug fixes

* Elixir: allow pairs to be ellipsis by @dimitris-m in #181; now patterns such as `%{..., some_item: $V, ...}` work as expected.

**Full Changelog**: https://github.com/opengrep/opengrep/compare/v1.1.0...v1.1.1


## [1.1.0](https://github.com/opengrep/opengrep/releases/tag/v1.1.0) - 31-03-2025

### New features

* Add support for reporting enclosure of matches by @maciejpirog in #169 and #178
* Resurrection of Elixir by @mbacarella and @dimitris-m in #150

### Details

There's now a new flag `--output-enclosing-context` that can be added to the `scan` command, adding information about the surrounding context of the matched fragments of code, such as the innermost function and/or class in which the match occurs.

This is only available for json output, so the `--json`flag must also be passed, and it's an experimental feature so it also requires `--experimental`.

Elixir support has been restored and will continue to be improved.

**Full Changelog**: https://github.com/opengrep/opengrep/compare/v1.0.2...v1.1.0


## [1.0.2](https://github.com/opengrep/opengrep/releases/tag/v1.0.2) - 24-03-2025

### Improvements

* Produce aarch64 linux binaries by @dimitris-m in #171
* Use opengrep's fork of semgrep-interfaces by @maciejpirog in #168

**Full Changelog**: https://github.com/opengrep/opengrep/compare/v1.0.1...v1.0.2


## [1.0.1](https://github.com/opengrep/opengrep/releases/tag/v1.0.1) - 19-03-2025

### Bug fixes

- Fix tree-sitter parsers for lisp, clojure and terraform in #166
- Pass jobs parameter to scan with --test in #164

### Improvements

- Pin Github actions to commit SHA in #162 and #163

### Contributors

@dimitris-m

**Full Changelog**: https://github.com/opengrep/opengrep/compare/v1.0.0...v1.0.1


## [1.0.0](https://github.com/opengrep/opengrep/releases/tag/v1.0.0) - 18-03-2025

### Highlights

- Windows support is now in beta, without any restrictions and with full parallelism enabled.
- Self-contained binaries for x86 Linux, arm64 Mac and x86 Windows.
- SARIF output has been re-enabled.
- Fingerprint and metavars fields are exposed again.

### Improvements

- Transitioned to OCaml 5.3.0, making use of the new multicore features.
- Timeouts and memory limits have been re-implemented and now they also work on Windows.
- Reduced memory footprint thanks to several optimisations.

### Contributors

@dimitris-m @mbacarella @madelinelawren @pritchyspritch @nir-valtman @maciejpirog @jesse-merhi @hansott @Kirill89 @HenriqueOCabral @willem-delbare

