# 构建哪吒探针FreeBSD二进制安装包

![构建哪吒探针FreeBSD二进制安装包](https://github.com/nezhahq/nezha/raw/master/.github/brand.svg)


![Os][os-shield]
[![Release][release-shield]][forks-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![Contributors][contributors-shield]][contributors-url]
[![License][license-shield]][license-url]


## 背景

由于哪吒探针官方未提供`FreeBSD`的二进制安装包，所以这里基于Github Actions来构建并将其上传到Github Release。

## 原理

`schedule.yml`的workflow文件：主要用于定时触发哪吒探针`FreeBSD`包的构建任务和定时清理构建记录。目前设定了北京时间8点、16点、24点这3个时间点触发构建。

`build.yml`的workflow文件：创建[vmactions/freebsd-vm](https://github.com/vmactions/freebsd-vm)虚拟机，然后拉取哪吒探针官方源代码，接着按照官方的构建步骤进行编译构建和打包发布。

## 用途

可在`serv00/ct8`这类FreeBSD OS上安装哪吒探针dashboard面板：[serv00和ct8主机一键安装哪吒探针和多主机保活](https://github.com/vfhky/serv00_ct8_nezha) 项目的dashboard面板下载地址就是来源于这里。

## Stars 趋势

[![Star History Chart](https://api.star-history.com/svg?repos=vfhky/nezha-build&type=Date)](https://star-history.com/#vfhky/nezha-build&Date)


<!-- links -->
[os-shield]: https://img.shields.io/badge/FreeBSD-blue
[release-shield]: https://img.shields.io/github/v/release/vfhky/nezha-build
[release-url]: https://github.com/vfhky/nezha-build/releases
[contributors-shield]: https://img.shields.io/github/contributors/vfhky/nezha-build
[contributors-url]: https://github.com/vfhky/nezha-build/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/vfhky/nezha-build?style=flat
[forks-url]: https://github.com/vfhky/nezha-build/network/members
[stars-shield]: https://img.shields.io/github/stars/vfhky/nezha-build?style=flat
[stars-url]: https://github.com/vfhky/nezha-build/stargazers
[issues-shield]: https://img.shields.io/github/issues/vfhky/nezha-build
[issues-url]: https://github.com/vfhky/nezha-build/issues
[license-shield]: https://img.shields.io/github/license/vfhky/nezha-build
[license-url]: https://github.com/vfhky/nezha-build/blob/master/LICENSE?color=blue
