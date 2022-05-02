# Elm_Compiler_0.19.1_for_aarch64
Elm compiler build for Linux ARM64(v8)

Official distribution does not support ARM yet.

### Download build -> https://github.com/Javier747Belbruno/Elm_Compiler_0.19.1_for_aarch64/releases/tag/v0.19.1


## Build (Only if you need for another arch)

1) Using a Docker.
https://gist.github.com/rlefevre/1523f47e75310e28eee243c9c5651ac9


2) Using normal flow.

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

## Sources

- https://github.com/elm/compiler/issues/2117
- https://github.com/elm/compiler/blob/master/installers/linux/README.md
- https://dev.to/csaltos/elm-for-linux-arm64-32bc


