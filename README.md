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
% asdf global reckoner 6.0.0
```

### With `ASDF_reckoner_OVERWRITE_ARCH`:

```
% ASDF_reckoner_OVERWRITE_ARCH=amd64 asdf install reckoner 6.0.0-rc.5
Downloading reckoner from https://github.com/FairwindsOps/reckoner/releases/download/v6.0.0-rc.5/reckoner_6.0.0-rc.5_darwin_amd64.tar.gz
% asdf global reckoner 6.0.0-rc.5
```

<!-- Begin boilerplate -->
## Join the Fairwinds Open Source Community

The goal of the Fairwinds Community is to exchange ideas, influence the open source roadmap,
and network with fellow Kubernetes users.
[Chat with us on Slack](https://join.slack.com/t/fairwindscommunity/shared_invite/zt-e3c6vj4l-3lIH6dvKqzWII5fSSFDi1g)
or
[join the user group](https://www.fairwinds.com/open-source-software-user-group) to get involved!

<a href="https://www.fairwinds.com/t-shirt-offer?utm_source=polaris&utm_medium=polaris&utm_campaign=polaris-tshirt">
  <img src="https://www.fairwinds.com/hubfs/Doc_Banners/Fairwinds_OSS_User_Group_740x125_v6.png" alt="Love Fairwinds Open Source? Share your business email and job title and we'll send you a free Fairwinds t-shirt!" />
</a>

## Other Projects from Fairwinds

Enjoying Polaris? Check out some of our other projects:
* [Goldilocks](https://github.com/FairwindsOps/Goldilocks) - Right-size your Kubernetes Deployments by compare your memory and CPU settings against actual usage
* [Pluto](https://github.com/FairwindsOps/Pluto) - Detect Kubernetes resources that have been deprecated or removed in future versions
* [Nova](https://github.com/FairwindsOps/Nova) - Check to see if any of your Helm charts have updates available
* [rbac-manager](https://github.com/FairwindsOps/rbac-manager) - Simplify the management of RBAC in your Kubernetes clusters

Or [check out the full list](https://www.fairwinds.com/open-source-software?utm_source=polaris&utm_medium=polaris&utm_campaign=polaris)
## Fairwinds Insights
If you're interested in running Polaris in multiple clusters,
tracking the results over time, integrating with Slack, Datadog, and Jira,
or unlocking other functionality, check out
[Fairwinds Insights](https://www.fairwinds.com/polaris-user-insights-demo?utm_source=polaris&utm_medium=polaris&utm_campaign=polaris),
a platform for auditing and enforcing policy in Kubernetes clusters.

<a href="https://www.fairwinds.com/polaris-user-insights-demo?utm_source=polaris&utm_medium=ad&utm_campaign=polarisad">
  <img src="https://www.fairwinds.com/hubfs/Doc_Banners/Fairwinds_Polaris_Ad.png" alt="Fairwinds Insights" />
</a>
