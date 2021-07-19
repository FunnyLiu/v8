# 源码分析


## 如何查看某个方法的源码


参考[如何在V8源码里找到某个JS方法是如何实现的？ - 知乎](https://www.zhihu.com/question/59792274/answer/168987086)



直接搜索`String.prototype.split`或者`Array.prototype.push`，基本都是c++获取tq完成的。

当然最好是结合着规范[ECMAScript® 2022 Language Specification](https://tc39.es/ecma262/#sec-array.prototype.push)





V8 JavaScript Engine
=============

V8 is Google's open source JavaScript engine.

V8 implements ECMAScript as specified in ECMA-262.

V8 is written in C++ and is used in Google Chrome, the open source
browser from Google.

V8 can run standalone, or can be embedded into any C++ application.

V8 Project page: https://v8.dev/docs


Getting the Code
=============

Checkout [depot tools](http://www.chromium.org/developers/how-tos/install-depot-tools), and run

        fetch v8

This will checkout V8 into the directory `v8` and fetch all of its dependencies.
To stay up to date, run

        git pull origin
        gclient sync

For fetching all branches, add the following into your remote
configuration in `.git/config`:

        fetch = +refs/branch-heads/*:refs/remotes/branch-heads/*
        fetch = +refs/tags/*:refs/tags/*


Contributing
=============

Please follow the instructions mentioned at
[v8.dev/docs/contribute](https://v8.dev/docs/contribute).
