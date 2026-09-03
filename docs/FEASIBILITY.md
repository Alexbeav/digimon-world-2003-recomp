# Digimon World 2003 release feasibility

Status: `bootstrap_verified`; four-platform `v0.3.5` package pending exact-package gates

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
