# asdf-polaris

[![Build Status](https://travis-ci.org/FairwindsOps/asdf-polaris.svg?branch=master)](https://travis-ci.org/FairwindsOps/asdf-polaris)

polaris plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

## Install

```
asdf plugin-add polaris https://github.com/FairwindsOps/asdf-polaris.git
```

## Use

Check out the [asdf documentation](https://asdf-vm.com/#/core-manage-versions?id=install-version) for instructions on how to install and manage versions of polaris.

## Architecture Override
The `ASDF_polaris_OVERWRITE_ARCH` variable can be used to override the architecture that is used for determining which `polaris` build to download. The primary use case is when attempting to install an older version of `polaris` for use on an Apple M1 computer as `polaris` was not built for ARM at the time.

### Without `ASDF_polaris_OVERWRITE_ARCH`:

```
% asdf install polaris 7.0.1
Downloading polaris from https://github.com/FairwindsOps/polaris/releases/download/7.0.1/polaris_darwin_amd64.tar.gz
```

### With `ASDF_polaris_OVERWRITE_ARCH`:

```
% ASDF_polaris_OVERWRITE_ARCH=amd64 asdf install polaris 7.0.0
Downloading polaris from https://github.com/FairwindsOps/polaris/releases/download/7.0.0/polaris_darwin_amd64.tar.gz
```

