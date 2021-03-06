# Knife Azure

[![Gem Version](https://badge.fury.io/rb/knife-azure.svg)](https://rubygems.org/gems/knife-azure) [![Build Status](https://travis-ci.org/chef/knife-azure.svg?branch=master)](https://travis-ci.org/chef/knife-azure)

## Description

A [knife] (<http://docs.chef.io/knife.html>) plugin to create, delete, and enumerate [Microsoft Azure] (<https://azure.microsoft.com>) resources to be managed by Chef.

NOTE: You may also want to consider using the [azure-xplat-cli](https://github.com/Azure/azure-xplat-cli), this application is written by the Azure team and has many other integrations with Azure. If click [here](https://github.com/chef-partners/azure-chef-extension/blob/master/examples/azure-xplat-cli-examples.md) you'll see deeper examples of using the Chef extension and Azure.

## Installation

Be sure you are running the latest version of Chef DK, which can be installed via:

```
https://downloads.chef.io/chef-dk/
```

This plugin is distributed as a Ruby Gem. To install it, run:

```bash
chef gem install knife-azure
```

Depending on your system's configuration, you may need to run this command with root/administrator privileges.

## Modes

`knife-azure 1.6.0` onwards, we are adding support for Azure Resource Manager. You can easily switch between the

- Service management: commands using the Azure service management API
- Resource manager: commands using the Azure Resource Manager API

They are not designed to work together. Commands starting with `knife azure` use ASM mode, while commands starting with `knife azurerm` use ARM mode.

PLEASE NOTE that `Azuererm` subcommands are experimental and of alpha quality. Not suitable for production use. Please use ASM subcommands for production.

## Configuration

1. [ASM Configuration] (docs/configuration.md#asm-mode)
2. [ARM Configuration] (docs/configuration.md#arm-mode)

## Detailed Usage

1. [ASM Mode] (docs/ASM.md)
2. [ARM Mode] (docs/ARM.md)

## Bootstrap existing VM to install the chef-client using chef-extension :

We have added a utility in ASM and ARM to bootstrap existing VM. This will install the chef-client using chef extension on your VM.

1. [Bootstrap Doc for ASM Mode] (docs/bootstrap.md#asm-mode)
2. [Bootstrap Doc for ARM Mode] (docs/bootstrap.md#arm-mode)

## Contributing

For information on contributing to this project see <https://github.com/chef/chef/blob/master/CONTRIBUTING.md>

## License

Copyright:: Copyright (c) 2012-2016 Chef Software, Inc.

License:: Apache License, Version 2.0

```text
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
