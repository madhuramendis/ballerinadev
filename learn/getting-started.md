---
layout: ballerina-inner-page
title: Getting Started
---

# Getting Started

## Download the Ballerina distribution

You can download the Ballerina distribution from [download page](https://ballerina.io/downloads/) for your operating system.

If a binary distribution is not available for your combination of operating system and architecture, try [installing from source](https://github.com/ballerina-platform/ballerina-lang#install-from-source).

### System requirements

Ballerina binary distributions are available for the following supported operating systems and architectures. Ensure that your system meets the requirements before you proceed with the installation.

- Windows Vista SP2 x64 or later
- Ubuntu Linux 12.04 x64 - LTS and above
- OS X 10.8.3 x64 and above

If your operating system or architecture is not on the list, you can [install from source](https://github.com/ballerina-platform/ballerina-lang#install-from-source).

## Installing Ballerina via installers

If you are upgrading to a new version of Ballerina from an older version, you can download and use the installer for the latest version. The installer will automatically uninstall the old version. 
If you are building from source, you must update the path with the new version of Ballerina.

### Installing on OS X

[Download the package file](/downloads) and double-click on it to launch the installer. The installer guides you through the installation process and installs the Ballerina distribution to `/Library/Ballerina`.

The package automatically sets your PATH environment variable for you. You may need to restart any open Terminal sessions for the change to take effect.

### Installing on Windows

[Download the MSI file](/downloads) and double-click on it to launch the installer. The installer guides you through the installation process and installs the Ballerina distribution to `C:\Program Files\Ballerina\`.

The installer should put the `C:\Program Files\Ballerina\<ballerina-directory>\bin` directory in your PATH environment variable. You may have to restart any open command prompts for the change to take effect.

### Installing on Linux

* [Download](/downloads) the latest version of Ballerina.

* If you downloaded the DEB file, use the following command to install Ballerina. Replace `<ballerina-home>/<ballerina-binary>.deb` with the actual file path. This installs Ballerina to the `/usr/lib/ballerina` directory.

```
dpkg -i <ballerina-binary>.deb
```

## Uninstalling Ballerina

To remove an existing Ballerina installation, go to the Ballerina installation location and delete the Ballerina directory.

> **Note**:
> - The installation location is usually `/Library/Ballerina` in Mac OS X, `/usr/lib/ballerina/` in Ubuntu and `C:\Program Files\Ballerina\` in Windows.

## Getting help

To get help when you work with Ballerina, see the [help page](/help).

## What's next

Once you have successfully installed Ballerina, try out the [Quick Tour](/learn/quick-tour) and take Ballerina for its first spin.
