# ggml-s-llama.cpp-precompiles
These are the precompiled binaries of the ggml-org/llama.cpp project , Just clone this repo and use , OS Used was: Ubuntu 24.04.02 LTS
Compiled by darkyboys at: Jul 24 2024 , 13:00 IST

### System Requirements

- 64-bit Linux OS
- glibc 2.34 or higher
- CPU with AVX2 and FMA support

### Building from source instructions
Run these commands if you want to build from source , These will efficiently build the ggml-org's llama.cpp but these are written by me and are not the official build instructions so for any issues don't blame ggml-org
```bash
git clone https://github.com/ggml-org/llama.cpp
cd llama.cpp
cmake . -DLLAMA_CURL=OFF
make -j`nproc`
cd bin
ls
```

These commands needs you to have `git`, `nproc`, `cmake` and `make` already installed on a `busybox` based linux distro. Once builded they you should see the list of all the builded files on your CLI, Othervise there is some problem while building.
