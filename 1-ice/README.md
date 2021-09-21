#Created by Rafael Guimarães Pereira - 21.Sep.2021

Example 1: Water to ice 

Copy the files to the local directory. You could point to the fftool script directory as so on but I prefer this way for didactic purposes.
For this example you’ll need the water molecule (spce.zmat) as well as its force field parameters (spce.ff). Copy also the fftool python script to the working directory.
You want to make a box with 200 water molecules with a density of 18 mol/L. Therefore you could to:
./fftool 200 spce.zmat -r 18
With this you have generated the ‘pack.inp’ file you are going to use along with Packmol
Look at the file typing:
less pack.inp
You are gonna obtain something like this:

# created by fftool
tolerance 2.5
filetype xyz
output simbox.xyz

structure spce_pack.xyz
  number 200
  inside box 1.5000 1.5000 1.5000 24.9244 24.9244 24.9244
end structure
pack.inp (END)
The xyz values are given in A. The software gives a space of 1.5A among each wall limit to avoid molecules overlapping. 

For further information about Packmol options and possibilities we encorage you to take a look at the given Github repository site (https://github.com/m3g/packmol).

Now copy the packmol program to your working directory.
Run: 
./packmol < pack.inp
With this command you assemble the simulation box, here named simbox.xyz
Now we need the topology files in order to run either with Gromacs or Lammps. For this example we are choosing Gromacs. Run the following command:
./fftool 200 spce.zmat -r 18 -g 
As a result of this command you’ll have generated 3 files:
field.top - the topology file (forcefield)
run.mdp - the ‘recipe file’ (temperature, pressure, steps, etc)
config.pdb - the atoms positions file


Figure 1: box composed of 200 water molecules.


For this simple example we are just doing a minor modification later.

> gmx grompp -f run.mdp -p field.top -c config.pdb

This command compiles the simulation files into the binary file ‘topol tpr’.
