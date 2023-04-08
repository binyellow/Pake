### 代码树结构

```bash
├── app.csv
├── bin
├── cli.js
├── dist
│   └── cli.js
├── icns2png.py
├── package.json
├── pake-default.icns
├── script
├── src-tauri
│   ├── assets
│   ├── build.rs
│   ├── Cargo.lock
│   ├── Cargo.toml
│   ├── icons
│   ├── png
│   ├── src
│   ├    ├──main.rs
│   ├    ├──app
│   ├    └──inject
│   ├── pake.json
│   ├── tauri.conf.json
│   ├── tauri.linux.conf.json
│   ├── tauri.macos.conf.json
│   └── tauri.windows.conf.json
└── tsconfig.json
```

### 文件说明
- app.csv：用于 bash/bat 命令批量替换打包。
- bin：采用 TypeScript 编写，为 pake-cli，即 pake 命令行打包工具的源码，可以使用`npm run cli:build`来生成最终配置文件`dist\cli.js`。
- cli.js：pake-cli 的入口文件，该文件调用`dist\cli.js`文件，基本不用修改，可以忽略。
- dist\cli.js：由`npm run cli:build`生成。
- icns2png.py：python3 编写，用于将 Mac 默认的 icns 图标转化为 windows/Linux 的 ico 与 png 格式图标。
- package.json：npm 模块依赖配置文件，运行`npm i`与`npm run xxx`时候需要用到该文件，用于构建基础开发环境。
- pake-default.icns：pake 默认的图标，适用于 MacOS。
- script：用于批量打包多个 app 的脚本，内置了[sd](https://github.com/chmln/sd)二进制包。可以用`npm run build:all-unix`和`npm run build:all-windows`分别调用 Mac/Linux 与 Windows 的批量打包功能。
- src-tauri/assets：储存了一个 Linux 的 desktop 图标配置文件和 Windows msi 安装配置文件。
- src-tauri/build.rs：tauri 编译入口，基本不用修改，可忽略。
- src-tauri/Cargo.lock：cargo 包管理配置结果文件，可忽略。
- src-tauri/Cargo.toml：cargo 包依赖配置文件，用于管理各个 crate 版本信息，基本不用修改，可忽略。
- src-tauri/icons：储存了一系列 icns 格式的图标文件，适用于 MacOS 应用图标。
- src-tauri/png：由上面的 icons 文件夹生成，储存了 ico 与 png 格式文件，适用于 Linux/Windows 的应用图标。
- src-tauri/src/main.rs：主程序文件，需要修改程序，跨平台移植方案，此外还可以查看 app 文件夹。
- src-tauri/src/inject：主程序文件配套的 js/css 注入代码，用于添加快捷键监听，页面渲染效果等等。
- src-tauri/pake.json：主配置文件，用于控制包名，版本号，打开链接，窗口大小等等。
- src-tauri/tauri.linux.conf.json：Linux 平台编译时用到的配置文件，包含 Linux 专用图标，维护者，二进制格式，映射相关等等。
- src-tauri/tauri.macos.conf.json：MacOS 平台编译时用到的配置文件，包含 MacOS 专用图标，维护者，二进制格式等等。
- src-tauri/tauri.windows.conf.json：Windows 平台编译时用到的配置文件，包含 Windows 专用图标，维护者，二进制格式，左上角小图标映射相关等等。
- tsconfig.json：TypeScript 配置，基本不需要修改，可忽略。
