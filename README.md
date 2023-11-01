# common-mujoco-errors
This is a repository intends to summarise common errors people encounter while setting up mujoco_py experiments.
-----
Keywords | Solved? 
--- | --- 
GL/glew.h | ✅
libcusolver | ✅
ffmpeg | ❌
CompileError | ✅
cython 3 | ✅


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

#### CompileError
`distutils.errors.CompileError: command '/GCCcore/11.3.0/bin/gcc' failed with exit code 1`

Solution: module load GCC/8.3.0

Comments: the loaded gcc cannot correctly compile the file, so we need to load the right version. 

-----

#### cython 3
`Mujoco-py is incompatible with cython 3 (Cannot assign type 'void (const char *) except * nogil' to 'void (*)(const char *) noexcept nogil)`

Solution: `pip install "cython<3"`

Comments: 

-----
