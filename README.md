# GN示例工程

## 关键目录结构如下

```
gn_demo
├─ .gn
├─ build
│  ├─ BUILDCONFIG.gn
│  └─ toolchain
│     └─ BUILD.gn
├─ BUILD.gn
├─ main.cc //测试cpp
├─ README.md
└─ third_party //第三方库
   └─ serial
      ├─ BUILD.gn
      ├─ impl
      │  ├─ unix.h
      │  └─ win.h
      ├─ serial.h
      ├─ src
      │  ├─ impl
      │  │  ├─ list_ports
      │  │  │  ├─ list_ports_linux.cc
      │  │  │  ├─ list_ports_osx.cc
      │  │  │  └─ list_ports_win.cc
      │  │  ├─ unix.cc
      │  │  └─ win.cc
      │  └─ serial.cc
      └─ v8stdint.h

```

## 必备文件
.gn

BUILD.gn

build/BUILDCONFIG.gn

build/toolchain/BUILD.gn

buildtools //gn和ninja工具（windows版本）

## 存在问题
目前只在Linux系统测试成功。window系统需要重写编译工具链（build/toolchain/BUILD.gn）