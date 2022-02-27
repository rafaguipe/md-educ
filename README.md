# md-educ

## Objective
Repository containing molecular dynamics exercises in order to teach students the basis of MD simulations using mostly Gromacs and Lammps as well as simple analysis.

## Dependencies
- Gromacs and/or Lammps, the new stable version the better.
- Packmol, https://github.com/m3g/packmol. Follow the installation instructions of this repository. 
- Fftool: https://github.com/paduagroup/fftool
- VMD: https://www.ks.uiuc.edu/Research/vmd/vmd-1.9.3/. You may use Pymol or another molecular visualization software but here we'll focus on VMD
- 

## Installation/disclaimer
There are different methods for you to install either Gromacs or Lammps. Advanced users more likely prefer to compile the code adding up specific options to match specific needs. For our educational purpose here we will teach you the most basic ways to accomplish a basic installation. Even though you may eventually experience some difficulties to do so depending on your operational system or hardware. In any case we do not provide any support or debug of any type for any software, package or dependencies here cited. You should install and sort out any eventual problem on your own, using the proper support or community channels. You may want to get know:

https://manual.gromacs.org/documentation/ 
https://docs.lammps.org/#

## Conda
We encourage you to install condar or miniconda and work with environments. This procedure will ensure you to keep consistency of software versions.
https://docs.conda.io/en/latest/miniconda.html

## Linux
In spite of the fact that you can work on any operating system, we encourage you to work with linux. If not yet, at some point of your career as scientist you will meet HPC (High Performance Computation) supercomputers and most of them run under some sort of Linux.

Mac terminal is similar but not the same as Linux. It will work fine most of the time.

Windows, you can work on xxx and there is MobaXTerm which I like https://mobaxterm.mobatek.net/.

Virtual Machines. You can use Linux inside your Mac or Windows under a VM. I've used the Oracle on https://www.virtualbox.org/ and works just fine. Depending on your machine configuration you may experience less performance, you have to try it out.

Which is my set-up: I use the Mac terminal to access HPC and also have Gromacs, Lammps, VMD and a bunch of Github repositories installed. Works fine. Because this Mac is a bit old and the OS is outdated I keep a second SSD with Linux installed and the dual book allows me to switch from one to another OS. I also have a PC running under Windows 10 and use MobaXTerm there, I find it handy you can do ssh and sftp on the same screen.

## Previous knowledge
We’ll assume you are a newby with no previous knowledge whatsoever about any of the tools hereby mentioned. Therefore we’ll guide you through but in many cases we left references so you deep dive by yourself. 

## Exercices
For the exercises you are going to use the Bash Terminal (whatever OS you have) and command line instructions, unless said otherwise.
Instructions for each exercise you find inside the respective directory.

