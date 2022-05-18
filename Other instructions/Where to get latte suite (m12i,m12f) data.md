
# 1. Stampede shared files
  
  ## For m12i or m12f (see file paths)

If you need to transfer to another system/cluster: Run this where the dot is to place it in the current folder on your system (use scopy instead of rsync)

`rsync -avz --progress tg876846@stampede2.tacc.utexas.edu:/scratch/projects/xsede/GalaxiesOnFIRE/metal_diffusion/m12i_res7100/output/snapdir_600 .`

Note that this should not be overused as rsync can cause problems for stampede.

The old method was:
`/scratch/projects/xsede/GalaxiesOnFIRE/metal_diffusion/m12f_res7100/output/snapdir_600`


 - stampede2 directory 

	`/scratch/projects/xsede/GalaxiesOnFIRE/metal_diffusion/`

 - Use medium resolution 7100, example for m12f:

	`m12f_res7100/output/`
	
- Use z=0 snapshot which is most recent one (600)	
	
	`/snapdir_600`



# 2. On the ananke site
should be at website
`ananke.hub.yt`

which in fact redirects to
`https://girder.hub.yt/#collection/5b0427b2e9914800018237da`

# Make sure you get all (4) components of a single snapshot
