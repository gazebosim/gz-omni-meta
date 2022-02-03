This is a meta repo containing the workspace and instructions to build `ign-omni`.

## Requirements

* colcon
* vcs
* cmake
* make
* g++

## Building

Get the sources
```bash
vcs import src < repos.yaml
```

Apply patches
```bash
git -C src/protobuf apply ../../protobuf-cmake.patch
```

Build

```bash
colcon build --merge-install --packages-up-to ignition-omni1
```

**Note:** `ignition-omni` will be built under `src/ign-omni/_build`, this is because it uses a custom build system by nvidia which is hard coded to put output in that directory.
