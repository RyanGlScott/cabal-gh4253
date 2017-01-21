# cabal-gh4253
A minimal example that showcases Cabal bug #4253

## Steps to reproduce

```
$ cabal install package1/ package2/
$ ghci -XPackageImports
GHCi, version 8.0.2: http://www.haskell.org/ghc/  :? for help
Loaded GHCi configuration from /home/rgscott/.ghci
λ> import "package1" DuplicateModuleName
λ> Window

<interactive>:1:1: error:
    Ambiguous interface for ‘DuplicateModuleName’:
      it was found in multiple packages:
      package1-0.1.0.0 package2-0.1.0.0
```
