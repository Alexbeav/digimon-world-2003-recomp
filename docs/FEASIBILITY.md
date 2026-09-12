# Digimon World 2003 release feasibility

Status: `bootstrap_verified`; four-platform `v0.3.6` package pending exact-package gates

The operator confirmed that the promoted private build reaches gameplay. This
meets the `bootstrap_verified` boundary. The source-only Windows package
builds locally. It must still pass exact-package setup, startup, and remote-byte
gates before public release.

The supported serial set is `SLES-03936`. The package uses
the owned-input distribution model. The player supplies the supported disc set
and BIOS, and the setup host builds the playable executable locally.

The package must not contain a disc, retail BIOS, generated retail code, save, capture,
prebuilt playable executable, or private absolute path.

## v0.3.3 executable-name correction

Public `v0.3.0` can complete a build and then request the wrong executable.
The corrected source uses `Digimon_World_2003_Recompiled` for CMake, the setup relaunch, and packaging.
The 24-title source parity gate passes. An exact-ZIP automatic-relaunch canary
must pass before release authorization.

## v0.3.5 three-platform refresh

The candidate targets Windows x64, Linux x64, macOS Apple Silicon ARM64, and
macOS Intel x64. The setup package uses an additive framework correction that
excludes two non-SDK helpers with developer-machine paths. Each exact package
must pass the payload, setup, startup, responsiveness, and clean-exit gates on
its declared platform before publication.

## 2026-09-03 portable Linux package

The release workflow now builds Linux in a pinned Ubuntu 20.04 container.
The package gate rejects a setup host or emitter that needs a glibc version
newer than 2.31. This keeps the release compatible with the qualified Rocky
Linux 9 host. Windows and both macOS builds keep their existing runners.

## 2026-09-04 v0.3.6 POSIX setup-copy candidate

This candidate pins PSXRecomp 08ec704a974b1f3a16335b4afeb340b9eff19926 and recomp-ui be8ac1d03ee19d55394b5a5f2d9d1506edd56659.
Linux and macOS packages use native CMake, Ninja, Python, C, and C++ tools.
Windows keeps the portable toolchain route. This change does not change game
code or the graduation state. Build-only CI and every exact-package release
gate must pass before publication.
