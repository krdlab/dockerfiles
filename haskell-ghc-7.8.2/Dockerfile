#
# GHC 7.8.2
#
# Author: krdlab
# Date: 2014/04/29

# $ sudo docker.io build -t yourname/ghc-7.8.2

FROM ubuntu:latest

RUN apt-get install -y build-essential wget make zlib1g-dev libgmp-dev libgmp3-dev

## GHC 7.8.2 official

RUN wget https://www.haskell.org/ghc/dist/7.8.2/ghc-7.8.2-x86_64-unknown-linux-deb7.tar.bz2
RUN tar xvfj ghc-7.8.2-x86_64-unknown-linux-deb7.tar.bz2
RUN cd ghc-7.8.2 && ./configure && make install
RUN rm -rf ghc-7.8.2*

RUN ghc --version

## cabal-install

RUN wget https://hackage.haskell.org/package/cabal-install-1.20.0.0/cabal-install-1.20.0.0.tar.gz
RUN tar xvfz cabal-install-1.20.0.0.tar.gz
RUN cd cabal-install-1.20.0.0 && sh ./bootstrap.sh
RUN rm -rf cabal-install-1.20.0.0*

# export PATH=$PATH:/.cabal/bin
