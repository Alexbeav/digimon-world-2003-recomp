# Development log

## 2026-09-01 — setup executable-name parity

The public `v0.3.0` source used different CMake and setup-relaunch executable
names. The corrected source uses `Digimon_World_2003_Recompiled` in all three title-owned paths.
`Test-SetupExecutableNameParity.ps1` passes. Exact-ZIP automatic relaunch is
still required before release.

## 2026-09-04 v0.3.6 POSIX setup-copy candidate

This candidate pins PSXRecomp 08ec704a974b1f3a16335b4afeb340b9eff19926 and recomp-ui be8ac1d03ee19d55394b5a5f2d9d1506edd56659.
Linux and macOS packages use native CMake, Ninja, Python, C, and C++ tools.
Windows keeps the portable toolchain route. This change does not change game
code or the graduation state. Build-only CI and every exact-package release
gate must pass before publication.

## 2026-09-13 - Reconcile published source into main

The default branch now includes the published v0.3.6 source. The release workflow uses the existing PSX-PUB-031 indentation repair. Later catalog identities and the current recomp-ui repository URL are preserved. The pinned runtime and UI commits match v0.3.6. No new package, release, gameplay test, or source-pin promotion is claimed.

Corpus consulted: PSX-PUB-031 and FAIL-142. The existing audit_release_workflow.py parser and regression supply the repair. Primary reference: https://github.com/softprops/action-gh-release documents overwrite_files under with. Source checks cover YAML structure, Actionlint, title executable-name tests when present, manifest versions, and exact release gitlinks.
