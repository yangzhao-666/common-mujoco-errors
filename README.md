# common-mujoco-errors
This is a repository intends to summarise common errors people encounter while setting up mujoco_py experiments.
-----
Keywords | Solved? 
--- | --- 
GL/glew.h | ✅
libcusolver | ✅
ffmpeg | ❌



-----
#### GL/glew.h
`fatal error: GL/glew.h: No such file or director`

Solution: if you are working with HPC, you need to `module load FFmpeg`. Otherwise, you need to install `mesa-libOSMesa-devel, mesa-libGL-devel, mesa-libGLU-devel`

Comments:

-----

#### libcusolver
`Could not load dynamic library 'libcusolver.so.10'`

Solution: If you don't have `sudo`, you can download `libcusolver.so.10` by running `cudatoolkit=11.0.3` (it is included in 11.0.3), then `~/ -iname libcusolver.so.10` to find the path of `libcusolver.so.10`. Add the returned path to your `bashrc`.


Comments: 

-----

#### ffmpeg
`No such file or directory: 'ffmpeg'`

Solution: 

Comments:

-----
