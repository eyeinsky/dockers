FROM debian:testing
RUN apt-get update && apt-get install -y libssl-dev ghc cabal-install && apt-get clean
RUN cabal update && cabal install base mtl bytestring text lens optparse-applicative template-haskell
RUN cabal install warp blaze-html
