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

In Case the upper commands takes soo long to build then use these commands, These are very fast but you will need `unzip` and `wget` already installed on your system.

```bash
wget https://github.com/ggml-org/llama.cpp/archive/refs/heads/master.zip
mkdir llama.cpp
unzip master.zip -d llama.cpp
cd llama.cpp
cmake . -DLLAMA_CURL=OFF
make -j`nproc`
cd bin
ls
```

Here you don't need `git` because we used the `github` download API to download the repository's master branch only. This drastically reduces the download time but only if you have all the dependencies already installed , If you have any issues with both build options then use this repository's pre-built binaries to avoid the compiling step.
