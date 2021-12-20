## Trinity: Desirable Mobile Emulation through Graphics Projection

![version](https://img.shields.io/badge/Version-Beta-yellow "Beta")
![license](https://img.shields.io/badge/GuestOS-Androidx86-green "Android")
![license](https://img.shields.io/badge/Licence-Apache%202.0-blue.svg "Apache")


### Table of Content

* [Introduction](#Introduction)
* [Codebase](#Codebase)
* [Install and Run](#Install and Run)
  * [Prerequisites](#Prerequisites)
  * [Running](#Running)
* [Measurement Data](#Measurement Data)

### Introduction

Trinity is the first mobile emulator that simultaneously achieves excellent compatibility, efficiency and security. 

Trinity is built on our novel concept of a *graphics projection space* that resides in the guest memory, where we selectively maintain a “projected” subset of control contexts and resource handlers that are actually required by the host GPU during its rendering, so as to minimize
the coupling between the guest-side and host-side graphics processing and thus keep the guest-host control/data flows *concise, smooth, and straight*.

This repository contains code and binary of Trinity, as well as measurement data involved in our study.

### Codebase

*Currently we are scrutinizing the codebase to avoid possible anonymity violation. This may take a while as the codebase is quite large (>100K LoC). We will release Trinity's code in a module-by-module manner as soon as we have finished examining a module and acquire its release permission from the authority.*

The released part can be found [here](https://github.com/TrinityEmulator/TrinityEmulator).

### Install and Run

We have released Trinity's binary for you to check out on your own PC [here](https://drive.google.com/drive/folders/1-2s3oKei5XgpkhVPKF8quxxWTwWctm5-?usp=sharing) (Window+Intel version, other versions such as Mac and AMD are coming soon as we are doing minor bug fixes). Some prerequisites and instructions are listed below.

#### Prerequisites

1. Ensure that you have turned on Intel VT in the BIOS settings.
2. Install Intel HAXM (instructions [here](https://github.com/intel/haxm/wiki)).

And then you are good to go!

#### Running

We provide an automatic script for running Trinity. Therefore, all you need to do is download the guest system's ISO, Trinity binaries and Batch file we provide, and double-click on the Batch file `run.cmd` to execute Trinity.

During booting, you may see an option to run without installation or to install provided by the Android-x86 system we host. The former allows you to quickly enjoy the journey but makes the virtual storage volatile (i.e., the next boot will erase all data), while the latter may involve more complex configurations (you can find them [here](https://www.android-x86.org/installhowto.html)).

#### Measurement Data

The measurement data involved in our evaluation are hosted [here](https://drive.google.com/drive/folders/1OjvQdG02EX8Wx1TlncvO0fk888q1k5Mg?usp=sharing).
