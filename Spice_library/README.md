# Create the library required for the project

You can download the library files given above or you can clone it as follows.

## What to download

- Clone the library [https://github.com/google/skywater-pdk-libs-sky130_fd_pr](https://github.com/google/skywater-pdk-libs-sky130_fd_pr) using the `git clone https://github.com/google/skywater-pdk-libs-sky130_fd_pr.git` command.
- Create a new file with the name "**sky130nm.lib**".
- Go to "cells" folder in the cloned directory and copy the files "sky130_fd_pr__pfet_01v8__tt.pm3.spice" and "sky130_fd_pr__nfet_01v8__tt.pm3.spice"
- "tt" means that the libraries are for typical corner.
- Now go to "models" folder in the cloned directory and copy the files "lod.spice" and "invariant.spice"
- **All the copied files must pasted next to "sky130nm.lib"**
- In the file sky130nm.lib, write the following code:

```
*sky130nm (tt) library
.include sky130_fd_pr__nfet_01v8__tt.pm3.spice
.include sky130_fd_pr__pfet_01v8__tt.pm3.spice
.include invariant.spice
.include lod.spice
```

