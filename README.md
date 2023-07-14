# occt-sys

Static build of OpenCascade packaged as a Rust Crate. To be used as a build dependency of crates that want to link OpenCascade statically. OpenCascade's header (include) files are also provided.

Note that this package *just* builds OpenCascade, it doesn't even instruct rustc to link its libraries. That is a responsibility of downstream crates.

## OCCT Build Configuration

Many features of OCCT are disabled at compile time (such as FFMPEG, OpenGL, Tcl, basically anything related to visualization or infrastructure). We can add cargo feature flags to enable these if there's interest.

## Building

* The `OCCT` codebase is included as a git submodule. Clone the repo with the `--recursive` flag, or use `git submodule update --init` to fetch the submodule.
