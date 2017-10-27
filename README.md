
项目说明
--------

**管理多个 repo ：**

- 单个 lint、build、test 和 release 流程
- 统一的地方处理 issue
- 不用到处去找自己项目的 repo
- 方便管理版本和 dependencies
- 跨项目的操作和修改变得容易
- 方便生成总的 changelog

安装
--------

```bash
npm install -g lerna # 全局安装工具，除了 Lerna,Builder，还可以像Andre Staltz 一样自己用脚本（通过Bash s）来实现 monorepo

lerna init # 初始化管理目录，同时之后手动配置子 package 间的调用关系：dependencies

lerna bootstrap # 会为各个 package 执行 npm install 所有的外部依赖；并为内部依赖的 package 建立 symlink,对所有的 package 执行 npm prepublish 

lerna publish # 发布到 npm
```