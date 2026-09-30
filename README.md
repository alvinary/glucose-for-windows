# glucose-for-windows

A MINGW-compatible fork of Glucose 4.2.1

This repository has the same contents as the Glucose (main repo)[https://github.com/audemard/glucose], with minimal edits to make it quickly compilable using MINGW on the Windows Linux Subsystem.

It also contains precompiled binaries, in the `bin-windows` directory, with a sample CNF file so you can quickly tests if everything's working well on your machine.

You should be able to recompile everything by running the following commands in a WSL terminal:

```bash
sudo apt install mingw-w64 libz-mingw-w64-dev cmake
unzip glucose-windows.zip && cd glucose-main
cmake -S . -B build-win -DCMAKE_TOOLCHAIN_FILE=mingw-w64-toolchain.cmake
cmake --build build-win -j$(nproc)
```

The WSL can be easily installed by following the instructions on its website.
