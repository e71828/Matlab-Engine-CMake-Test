Matlab-Engine-CMake-Test
========================

A small test to show that running Matlab code from CMake build c++ files is indeed possible.


[Reference](https://ww2.mathworks.cn/help/matlab/matlab_external/build-c-engine-programs.html)

## Add Matlab to System Path
`C:\Program Files\MATLAB\R2023a\extern\bin\win64`

| 操作系统 | 变量                | 路径                                                      |
| :------- | :------------------ | :-------------------------------------------------------- |
| Windows  | `PATH`              | `matlabroot\extern\bin\win64`                             |
| macOS    | `DYLD_LIBRARY_PATH` | `matlabroot/extern/bin/maci64`                            |
| Linux    | `LD_LIBRARY_PATH`   | `matlabroot/extern/bin/glnxa64:matlabroot/sys/os/glnxa64` |


## Potential gotcha's
Only run in MinGW bash.
