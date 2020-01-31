# The CovScript Manager Project

The man behind Covariant Script who maintains all versions, packages and lots of trivial stuffs for programmers.

**We call him `csman`.**

### 项目约定

- 语言标准：C++ 14（与 [CovScript](https://github.com/covscript/covscript) 主项目同步）
- 开发工具：任何支持 EditorConfig 的编辑器/IDE
- 开发模式：独立开发分支 -> PR -> Code Review -> 合并到主分支

### 开发计划

#### 平台
- [ ] Windows
    - [ ] MSVC [Experimental]
        - [ ] AMD64
        - [ ] i386,
        - [ ] ARM
    - [ ] MinGW-w64
        - [ ] AMD64 [Mainstream]
        - [ ] i386
- [ ] Linux
    - [ ] GCC
        - [ ] AMD64 [Mainstream]
        - [ ] i386
        - [ ] ARM
        - [ ] MIPS
- [ ] macOS
    - [ ] clang
        - [ ] AMD64 [Mainstream]

#### 功能

- [ ] 版本管理：支持安装多个 CovScript 版本，并支持设置默认版本
    - [ ] `csman install <latest | nightly | version> [--reinstall | --fix]`
    - [ ] `csman uninstall <all | version-regex> [--clean]`
    - [ ] `csman checkout <latest | version>`
    - [ ] `csman run [-v version] <command>`
    - [ ] `csman list`
- [ ] 扩展管理：全功能联网包管理器，支持分运行时版本进行管理
    - [ ] `csman install <package name> [--reinstall | --fix]`
    - [ ] `csman uninstall <package name(regex)> [--clean]`
    - [ ] `csman list`
- [ ] 配置管理：命令行配置管理器
    - [ ] `csman config set <key> <value>`
    - [ ] `csman config unset <key>`
    - [ ] `csman config get <key>`


#### 附加：CovScript 源定义

- 根目录
    - csman.info
        - Base Url:
        - Platform: [平台名称...]
    - 平台(`OS_Compiler_Architecture`, 如`Win32_MSVC_AMD64`)
        - csman.info
            - Base Url:
            - Version: [版本号...]
            - Latest: [版本号]
            - Nightly: [版本号]
        - 版本号(`Master.Major.Minor.Revise`, 如`2.3.3.3`)
            - runtime: 发行包(.csrtm)
            - develop: 开发包(.csdev)
            - package: 扩展包(.cspkg)

