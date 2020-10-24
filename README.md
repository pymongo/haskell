# Learn Haskell

一直很喜欢Rust中Trait的设计，想追根溯源看看Haskell的typeclass，好奇Haskell是如何影响Rust的

The way I learn Haskell is 《Learn You a Haskell for Great Good!》(Haskell趣学指南)，

我只看英文版，Google搜索"haskell tutorial"第一条搜索结果就是此书在线阅读的网站

## Haskell项目构建与工具介绍

### Haskell安装

和Rust一样，不建议通过brew安装"brew install ghc cabal-install"，建议使用类似rustup的ghcup安装

ghcup安装ghc时会自动安装上Haskell Language Server，这是VSCode的Haskell插件必备

ghc是最流行的Haskell编译器/解释器，cabal类似cargo的项目构建+包管理工具

### 运行一个Haskell程序的三种方法

另一款Haskell项目工具是stack，我作为初学者暂时就只用官方的cabal够了

1. cabal init && cabal run
2. runghc Main.hs # runghc是解释器不会编译代码
3. ghc Main.hs && ./Main

### vscode配置Haskell的开发环境(失败)

搞不懂明明ghcup已经安装了Haskel Language Server，为啥vscode插件报错没找到，又不提供自动安装的选项

然后我编译hie源码修改json配置指定路径，又报错hie跟系统的Haskell版本不对

插件就完全不能用

### ghci

ghci是类似irb的Haskell REPL工具，输入`:?`可以查看ghci REPL环境特有的一些命令

常用`:l Main.hs`加载一个源文件，然后直接输入main就可以调用main函数，我注意到":l"之后ghci的左侧的"Prelude>"会变成"*Main>"，可能进入Main模块/命名空间?

使用`:t putStrLn`看看cabal自动生成的Main.hs中类似"print"方法的函数putStrLn的入参返回值类型

