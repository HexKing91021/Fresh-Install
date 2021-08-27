# Fresh-Install
This repository should have everything you need to get started with a brand new installation of Windows.

# Base Boxstarter Installation

When you're ready to get started, follow the steps below and you'll be on your way to a new machine!

## Install Chocolatey

To install Chocolatey, run the following command in Powershell **as administrator:**
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

## Install Boxstarter
After you've installed chocolatey, you'll need to install Boxstarter:
```
cinst boxstarter
```

Now install the Boxstarter modules:
```
. { iwr -useb https://boxstarter.org/bootstrapper.ps1 } | iex; Get-Boxstarter -Force
```

## Finally
Now that everything is set up, we can start the installation of your programs:

```
Install-BoxstarterPackage -PackageName [insertLinkHere] -DisableReboots
```

The community package directory can be found [here](https://community.chocolatey.org/packages).
