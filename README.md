# Elm_Compiler_0.19.1_for_aarch64
Elm compiler build for ARM64(v8)

## Download build -> Go to Release


## Steps for Building (Steps I took to build it) 

```bash
sudo apt-get install -y build-essential \
    automake \
    autotools-dev \
    make \
    g++ \
    ca-certificates \
    software-properties-common \
    apt-transport-https \
    lsb-base \
    lsb-release \
    zlib1g-dev \
    libpcre3-dev \
    libcurl4-openssl-dev \
    libc-dev \
    libxml2-dev \
    libsnmp-dev \
    libssh2-1-dev \
    libevent-dev \
    libopenipmi-dev \
    libpng-dev \
    pkg-config \
    libfontconfig1 \
    git \
    bzip2 \
    zip \
    unzip \
    musl-dev \
    ghc \
    cabal-install \
    libmpfr-dev

git clone https://github.com/elm/compiler.git
cd compiler
git checkout 0.19.1

rm worker/elm.cabal
cabal new-update
cabal new-configure
cabal new-build

cd /dist-newstyle/build/aarch64-linux/ghc-8.6.5/elm-0.19.1/x/elm/build/elm
chmod +x elm
sudo mv elm /usr/local/bin/
```

Test if it works

```bash
elm --help
```
