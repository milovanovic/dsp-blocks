# A Collection of Digital Signal Processing Block Generators

[![Build](https://github.com/ucb-bar/dsp-blocks/actions/workflows/test.yml/badge.svg)](https://github.com/ucb-bar/dsp-blocks/actions/workflows/test.yml)

This repository contains a variety of Digital Signal Processing (DSP) accelerators designed in a configurable and modular fashion. Currently available are listed below:

 * **sdf-fft** - A Single-Path-Delay-Feedback (SDF) Fast Fourier Transform (FFT) hardware accelerators
 * **lis** - A Fully Streaming Linear Insertion Sorter (LIS) Design Generator
 * **magnitude** - A Design Generator of Complex Number Magnitude Calculators and their Logarithms
 ## Documentation

For the detailed documentation of each design generator, check directory `name_of_the_generator/doc/`.

 ## Setup

This project is intended to be used and run inside [chipyard](https://github.com/ucb-bar/chipyard) environment.  Anyhow, if you want to use this repository standalone then follow instructions below:

* Clone this repository.
* Switch directory.
* Initialize all tools and submodules.
* Switch to project (e.g. sdf-fft).
* Compile code, generate verilog or run tests.

```
git clone https://github.com/milovanovic/dsp-blocks.git
cd dsp-blocks
./scripts/init_submodules_and_build_sbt.sh
sbt project sdf_fft
sbt compile/run/test
```
#### Note

The shell script `init_submodules_and_build_sbt.sh`, initializes all tools and generators required to run this project. Besides that, it initializes `bulid.sbt` with all correctly defined dependencies. Versions of tools and generators correspond to the Chipyard 1.9.1 release. The user can replace versions by changing corresponding checkout commits inside the same script (this can influence some changes in source code as well). The shell script `remove_submodules.sh` executes commands that reverse the commands listed in `init_submodules_and_build_sbt.sh`.

## Guide For New Contributors

If you are trying to make a contribution to this project, please follow this guide:
1.  You can contribute by submitting pull requests from your fork to the upstream repository.
2.  If you need help on making a pull request, follow this [guide](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests).
3.  To understand how to compile and test from the source code, follow the instructions inside the setup section.
