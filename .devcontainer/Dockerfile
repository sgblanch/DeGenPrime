FROM debian:bookworm-slim

RUN set -eux; \
    apt-get update; \
    apt-get upgrade -y; \
    apt-get install -y --no-install-recommends build-essential clang cmake gdb git libclang-rt-dev-wasm32 libc++-dev-wasm32 lld lldb make ninja-build openssh-client; \
    printf "set(WASI 1)\n" > /usr/share/cmake-3.25/Modules/Platform/WASI.cmake; \
    git config --global core.autocrlf input; \
    git config --global color.ui auto
