# asdf-gonogo

[![Build Status](https://travis-ci.org/TheCubicleJockey/asdf-gonogo.svg?branch=master)](https://travis-ci.org/TheCubicleJockey/asdf-gonogo)

gonogo plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

## Install latest version of GoNoGo

```
asdf plugin-add gonogo https://github.com/TheCubicleJockey/asdf-gonogo.git
asdf install gonogo $(curl --silent "https://api.github.com/repos/FairwindsOps/gonogo/releases/latest" | jq ".. .tag_name? // empty")
```

## Use

Check out the [asdf documentation](https://asdf-vm.com/#/core-manage-versions?id=install-version) for instructions on how to install and manage versions of gonogo.

## Architecture Override
The `ASDF_GONOGO_OVERWRITE_ARCH` variable can be used to override the architecture that is used for determining which `gonogo` build to download. The primary use case is when attempting to install an older version of `gonogo` for use on an Apple M1 computer as `gonogo` was not built for ARM at the time.

### Without `ASDF_GONOGO_OVERWRITE_ARCH`:

```
% asdf install gonogo 0.2.1
Downloading gonogo from https://github.com/FairwindsOps/gonogo/releases/download/v0.2.1/gonogo_0.2.1_darwin_amd64.tar.gz
```

### With `ASDF_GONOGO_OVERWRITE_ARCH`:

```
% ASDF_GONOGO_OVERWRITE_ARCH=amd64 asdf install gonogo 0.2.0
Downloading gonogo from https://github.com/FairwindsOps/gonogo/releases/download/v0.2.0/gonogo_0.2.0_darwin_amd64.tar.gz
```

<!-- Begin boilerplate -->
## Join the Fairwinds Open Source Community

The goal of the Fairwinds Community is to exchange ideas, influence the open source roadmap,
and network with fellow Kubernetes users.
[Chat with us on Slack](https://join.slack.com/t/fairwindscommunity/shared_invite/zt-e3c6vj4l-3lIH6dvKqzWII5fSSFDi1g)
or
[join the user group](https://www.fairwinds.com/open-source-software-user-group) to get involved!


<a href="https://www.fairwinds.com/t-shirt-offer?utm_source=gonogo&utm_medium=gonogo&utm_campaign=gonogo-tshirt">

 <img src="https://www.fairwinds.com/hubfs/Doc_Banners/Fairwinds_OSS_User_Group_740x125_v6.png" alt="Love Fairwinds Open Source? Share your business email and job title and we'll send you a free Fairwinds t-shirt!" />
</a>

## Other Projects from Fairwinds


Enjoying ASDF-GoNoGo? Check out some of our other projects:

* [Polaris](https://github.com/FairwindsOps/Polaris) - Audit, enforce, and build policies for Kubernetes resources, including over 20 built-in checks for best practices
* [Goldilocks](https://github.com/FairwindsOps/Goldilocks) - Right-size your Kubernetes Deployments by compare your memory and CPU settings against actual usage
* [Nova](https://github.com/FairwindsOps/Nova) - Check to see if any of your Helm charts have updates available
* [rbac-manager](https://github.com/FairwindsOps/rbac-manager) - Simplify the management of RBAC in your Kubernetes clusters
* [GoNoGo](https://github.com/FairwindsOps/GoNoGo) - Simplify the management of RBAC in your Kubernetes clusters

Or [check out the full list](https://www.fairwinds.com/open-source-software?utm_source=gonogo&utm_medium=gonogo&utm_campaign=gonogo)