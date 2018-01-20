## 版本控制

版本控制是写代码时必不可少的一个环节。

> **版本控制**（**Revision control**）是维护工程[蓝图](https://zh.wikipedia.org/wiki/%E8%97%8D%E5%9C%96)的标准作法，能追踪工程蓝图从诞生一直到定案的过程。此外，版本控制也是一种[软件工程](https://zh.wikipedia.org/wiki/%E8%BB%9F%E9%AB%94%E5%B7%A5%E7%A8%8B)技巧，借此能在软件开发的过程中，确保由不同人所编辑的同一代码文件案都得到同步。

### Git 与 SVN

有两种类型的版本控制软件，中央式系统和分布式系统，两者的代表分别是 Git 与 SVN。关于两者利弊的讨论有一大堆，可以全部忽略掉，直接选用 Git，原因很简单，Git 在实际中使用越来越频繁，用途也更加广泛，不光编码，写论文、写文章、写书都可以方便地使用 Git，而 SVN 只见于多年前的大型软件系统。

> 分布式系统 [Linux 内核](https://zh.wikipedia.org/wiki/Linux%E5%85%A7%E6%A0%B8)的发明人[林纳斯·托瓦兹](https://zh.wikipedia.org/wiki/%E6%9E%97%E7%B4%8D%E6%96%AF%C2%B7%E6%89%98%E7%93%A6%E8%8C%B2)就是分布式版本控制系统的支持者，他开发了目前被开源社区广泛使用的分布式版本控制系统 [Git](https://zh.wikipedia.org/wiki/Git)。

### Git 命令

虽然每个操作系统都有 Git 图形化操作客户端，但仍然建议学习 Git 命令，使用几次熟练后，效率会大大提升。最常用的命令无非以下几个：

```shell
git clone
git add .
git commit 
git push 
git pull
git reset
git branch
```

快速掌握 Git 可以参考官方文档和[廖雪峰的教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000) 。

### 工作流

