# Bug Eradication Program

## Goal

Drive the repository toward **zero known reproducible unintended defects** for the selected Pokémon Sword target revision while preserving intended game rules, content, version differences, and patch-era behavior as documented evidence.

This program covers crashes, hangs, softlocks, progression blockers, save/data corruption, battle-logic defects, AI defects, invalid data, script/event errors, collision and map errors, graphics/UI/display errors, audio errors, localization/text errors, online/local communication defects, DLC interactions, performance defects, resource leaks, update regressions, and other reproducible unintended behavior.

## Target identity gate

No binary-specific fix is considered verified until `config/target.json` identifies the exact release/region/revision and cryptographic hashes of the locally supplied legal dump or extracted target. ROM/installable-package binaries are never committed.

## Evidence classes

- **Confirmed**: reproduced on the exact target or proven from extracted code/data with sufficient evidence.
- **Probable**: strong code/data evidence but reproduction is incomplete.
- **Reported**: externally documented report awaiting local reproduction.
- **Not a bug**: intended behavior, unsupported configuration, user/environment error, or disproven report.

## Severity

- **S0 Critical** — save corruption, unrecoverable progression loss, deterministic fatal crash affecting normal play.
- **S1 High** — softlock, major progression failure, severe battle/system logic break, frequent crash.
- **S2 Medium** — incorrect mechanics/data/event behavior with meaningful gameplay impact.
- **S3 Low** — visual/audio/text/UI/collision issues with limited gameplay impact.
- **S4 Cosmetic** — presentation-only defect with no functional impact.

## Required lifecycle

Every defect must pass through:

1. discovery and source citation;
2. target/revision assignment;
3. reproduction steps and expected/actual result;
4. evidence capture and root-cause location;
5. minimal fix or data correction;
6. build/patch output without committing a full game image;
7. positive regression test proving the defect is fixed;
8. negative regression tests proving nearby intended behavior is unchanged;
9. version/DLC compatibility checks;
10. final status `verified-fixed` only after all required tests pass.

## Sword-specific version axes

Track separately when applicable:

- base game versus Expansion Pass content;
- The Isle of Armor;
- The Crown Tundra;
- offline/local/online behavior;
- original release versus each supported update revision;
- region/language differences;
- Sword-only versus Shield-shared code/data behavior.

## Repository placement

- `manifests/bug-registry.json`: authoritative machine-readable defect index.
- `analysis/bugs/`: reproduction notes, root-cause reports, comparison material.
- `patches/bugs/`: patch material, diffs, address/symbol maps.
- `logs/bugs/`: execution and regression logs.
- `artifacts/bugs/`: retained non-ROM outputs and evidence.
- `tools/`: validators and automation.

## Completion rule

A revision is considered clean only when every known item in the registry is either `verified-fixed` or `not-a-bug`, all automated validations pass, and no unresolved `reported`, `probable`, `confirmed`, or regression item remains for that revision.
