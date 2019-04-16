
1. mac上rasterio编译报错：

```bash
g++ -bundle -undefined dynamic_lookup -L/Users/sshuair/anaconda3/envs/rasterio_swift/lib -arch x86_64 -L/Users/sshuair/anaconda3/envs/rasterio_swift/lib -arch x86_64 -arch x86_64 build/temp.macosx-10.7-x86_64-3.6/rasterio/_warp.o -L/Users/sshuair/anaconda3/envs/rasterio_swift/lib -lgdal -o build/lib.macosx-10.7-x86_64-3.6/rasterio/_warp.cpython-36m-darwin.so
clang: warning: libstdc++ is deprecated; move to libc++ with a minimum deployment target of OS X 10.9 [-Wdeprecated]
ld: library not found for -lstdc++
clang: error: linker command failed with exit code 1 (use -v to see invocation)
error: command 'g++' failed with exit status 1
```

解决方法：https://stackoverflow.com/questions/53287975/pybind11-doesnt-work-or-c-doesnt-compile-after-upgrading-to-mojave-lstdc

`export MACOSX_DEPLOYMENT_TARGET=10.9`
