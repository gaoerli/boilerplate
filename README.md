# 基于 FIS3 的前端工程模板

## 环境要求

要求 Node.js v4.0 及以上。

## 安装依赖

工程取消了原有的全局安装，所有依赖均在本地。进入工程目录，使用以下命令安装：

`npm i` 或 `yarn`

> 如遇网络环境不稳定，建议安装 `nrm`, 切换仓库后重试。执行安装 `npm i -g nrm` 或 `yarn global add nrm`。[查看手册](https://yarnpkg.com/zh-Hans/package/nrm)

## 运行开发环境

### 启动

使用 `npm run dev` 或 `yarn dev` 启动开发服务器，合并热刷新浏览器。默认运行于 [http://127.0.0.1:8080/]() 和 [http://\[本机 IP\]:8080/]() .

### 发布

使用 `npm run build` 或 `yarn build` 将产出输出至 `./dist` 文件夹。

## 提示与计划

- 新增 `media-srouces` 目录，用于存放 PSD 和 Ai 切图文件。
  > **注意：** 不要放置需求原始设计文件。
- 未来计划使用 `ES6` 模块写法，因为低版本兼容还未实现，姑且使用立即执行函数方法包裹。
- 样式与脚本文件，不要使用人名或缩写，坚持语义化。建议为每一个独立的功能（模块）新建相应文件。
- 不会引入 **模板引擎**，必要时使用 `ES6` 模板字符窜。

## IDE 集成

假设你正在使用 [VS Code](https://code.visualstudio.com/) .

- 安装 Prettier.

  在 `用户设置` 中启用自动保存，及保存时自动格式化。

  ```json
    "files.autoSave": "onFocusChange",
    "editor.formatOnSave": true,
    "javascript.format.enable": false // JavaScript 格式化将由 ESLint 接管。
  ```

- 安装 ESLint, 以启用 JavaScript 语法检查，及自动格式化。将使用 Prettier 配置。修改 `用户设置`：

  ```json
    "eslint.autoFixOnSave": true,
    "eslint.alwaysShowStatus": true,
    "eslint.enable": true,
    "eslint.packageManager": "yarn"
  ```

VS Code 有很多高效设置，[了解更多](https://github.com/Microsoft/vscode-tips-and-tricks)。
