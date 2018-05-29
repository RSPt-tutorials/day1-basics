# day1-basics
Introduction to RSPt and bcc Fe

## Introduction 

#### Manual
the manual of RSPt is stored in the folder [documentation/manual](documentation/manual/).
To obtain the manual in pdf format one needs to type:
````
latex manual.tex
````
three times.

#### RSPt's basis set
![Basis set visualization](basis_set_visualization.png "Visualization of RSPt's basis set")

#### RSPt simulation files 
To execute the `rspt` binary you need the following files:
- `data` (compound specific info, what atoms, basic functions, etc...)
- `spts` (information of the k-mesh)
- `atomdens` (information of the overlapping atomic density, which is used as a starting guess)
- `symcof` (Information about symmetries and basis)

An existing calculating also contains:
- `pot` (the potential)
- `eparm` (linearlization energies)

When setting up a calculation from scratch, one starts with *one* file called `symt.inp`.
It contains the basic information such as lattice vectors, lattice parameter and atom positions.
By typing: 
```bash
symt -all 
```
many of the files needed to run a simulation is created. Below follows a step-by-step description of how to setup a simulation of bcc Fe.

## bcc Fe
#### Preparations
Before using RSPt, make sure the same modules are loaded as when compiling RSPt.
E.g. on Rackham, type:
```
module load intel/18.1 intelmpi/18.1
```
A convinient way is to load the module automatically at login by putting the command in the `~/.bashrc` file.



