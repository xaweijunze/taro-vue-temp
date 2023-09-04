# taro-vue-router

本项目用于检验 Taro 项目使用 `vue-router` 开发多路由页面。

Taro v3.6 已发布，请直接使用 `"^3.6"` 版本体验本仓库内容。

## 如何开发

### Taro 仓库

1. 克隆 Taro 仓库: `git clone https://github.com/AdvancedCat/taro.git` ；

2. 安装依赖 `pnpm i`；

3. 切换至 `feat/history` 分支；

4. 编译包 `pnpm build`；

5. 将 `@tarojs/runtime` `@tarojs/mini-runner` 链接到全局

```bash
$ cd packages/taro-runtime
$ pnpm link --global
$ cd packages/taro-mini-runner
$ pnpm link --global
```


### 本仓库

1. 克隆本仓库：`git clone https://github.com/AdvancedCat/taro-vue-router.git`；

2. 安装依赖：`pnpm i`；

3. 链接包 `@tarojs/runtime` `@tarojs/mini-runner`；

```bash
$ pnpm link --global @tarojs/runtime
$ pnpm link --global @tarojs/mini-runner
```

4. 运行 `npm run dev:weapp`，在微信开发者工具中即可预览效果；

5. 请注意：
```
项目启动时报错：
taro-vue-router/node_modules/@tarojs/webpack5-runner/dist/plugins/MiniPlugin.js:410
throw new Error('全局配置缺少 pages 字段，请检查！');
```
```
上述问题解决方案：
    运行taro -v查看版本，修改package.json，将taro相关版本号全部替换为实际版本。
```