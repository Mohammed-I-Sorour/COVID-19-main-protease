# COVID-19-main-protease
COVID-19 main protease-6lu7 prepared for docking
In this file we will describe the process we followed to prepare the COVID-6LU7 protein for docking 

1-The 6lu7 protein was dowloaded from the protein data bank: https://www.rcsb.org/structure/6LU7
2-The 6lu7 is crystalized in th epresence of a covalently linked inhibitor, N3. 
3-I removed the inhibitor and capped the Cys-145 residue sulfer atom with a hydrogen. 
4-The the rest of the hydrogen of the sysytem were added. the water molecule that came as a part of the crystalized structure were removed. 
5-The most important step now is to relax the system after the removal of the covalently linked ligand. To do so, we ran 10ns equilibrium molecular dynamics to relax the system. 

MD relaxation details: 
The protein topology was built using CHARMM36 FF while the positively charged ligand need a different treatment where we built its topology using CHARMM General Force Field (CGenFF)1.  We solvated the system in a cubic simulation box using TIP3P waters and 150 M of NaCl. We ran the simulation at 310K and 1 atm in an NPT enesmble using the Leap-Frog integrator. We used the Particle Mesh Ewald for long-range electrostatics and Ewald cutoff distance of 15 angstroms. The simulation was ran for 50ns using GROMACS_2018.8. 

I will provide the pdb files of the system at 5 and 10 ns. The reason that I provide both of them is that the frame at 5 ns have been released earlier and is currently part of some research work. For future docking studies, I recommend using the ns structure. 
