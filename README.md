# asdf-reckoner

[![Build Status](https://travis-ci.org/FairwindsOps/asdf-reckoner.svg?branch=master)](https://travis-ci.org/FairwindsOps/asdf-reckoner)

reckoner plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

## Install

```
asdf plugin-add reckoner https://github.com/FairwindsOps/asdf-reckoner.git
```

## Use

Check out the [asdf documentation](https://asdf-vm.com/#/core-manage-versions?id=install-version) for instructions on how to install and manage versions of reckoner.

## Architecture Override
The `ASDF_reckoner_OVERWRITE_ARCH` variable can be used to override the architecture that is used for determining which `reckoner` build to download. The primary use case is when attempting to install an older version of `reckoner` for use on an Apple M1 computer as `reckoner` was not built for ARM at the time.

### Without `ASDF_reckoner_OVERWRITE_ARCH`:

```
% asdf install reckoner 6.0.0
Downloading reckoner from https://github.com/FairwindsOps/reckoner/releases/download/v6.0.0/reckoner_6.0.0_darwin_amd64.tar.gz
```

### With `ASDF_reckoner_OVERWRITE_ARCH`:

```
% ASDF_reckoner_OVERWRITE_ARCH=amd64 asdf install reckoner 6.0.0-rc.5
Downloading reckoner from https://github.com/FairwindsOps/reckoner/releases/download/v6.0.0-rc.5/reckoner_6.0.0-rc.5_darwin_amd64.tar.gz
```

