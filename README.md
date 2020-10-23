# Learn Haskell

一直很喜欢Rust中Trait的设计，想追根溯源看看Haskell的typeclass，好奇Haskell是如何影响Rust的

## Haskell项目构建与工具介绍

### Haskell安装

> brew install ghc cabal-install

ghc是最流行的Haskell编译器/解释器，cabal类似cargo的项目构建+包管理工具

### 运行一个Haskell程序的三种方法

1. cabal init && cabal run
2. runghc Main.hs # runghc是解释器不会编译代码
3. ghc Main.hs && ./Main

### ghci

ghci是类似irb的Haskell REPL工具
