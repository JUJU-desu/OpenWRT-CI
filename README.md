# 高质量<免费>交流群

# JUJU-desu / ZN M2 定制配置

当前 `QCA-ALL` 只编译兆能 M2 的无 Wi-Fi 精简固件：不包含 ath11k 无线、USB 总线/存储/网络模块、Samba4 或 HomeProxy。

Passwall2、OpenClash、EasyTier 使用 APK 模块包方式编译（`CONFIG_PACKAGE_*=m`），不会固化到 squashfs；构建产物中的 `.apk` 需要手动安装到 overlay，例如：

```sh
apk add /tmp/luci-app-passwall2-*.apk
apk add --upgrade /tmp/luci-app-passwall2-*.apk
```

升级固件时不要使用 `sysupgrade -n`，否则会清空 overlay 中手动安装的插件和配置。若想清理旧版本残留，可先执行 `apk del <package>` 再安装新包。

[IPQ技术讨论群](https://qm.qq.com/q/v7nMhzB4oU)

# 高质量<付费>中转站

[LiBwrt-Ai](https://api.zipimg.cn/register?aff=LR7FSZ2ZZ4D3)

# 本地编译器

https://github.com/VIKINGYFY/OWRT-Tools.git

# 自用修改版插件

https://github.com/VIKINGYFY/packages.git

# OpenWRT-CI

官方版：

https://github.com/immortalwrt/immortalwrt.git

自用版：

https://github.com/VIKINGYFY/immortalwrt.git

# U-BOOT

高通版-沉心：

https://github.com/chenxin527/uboot-qsdk12.5-build.git

高通版-小猪：

https://github.com/1980490718/u-boot-2016.git

联发科-全新版：

https://github.com/VIKINGYFY/UBOOT-CI/releases

联发科-官方版：

https://drive.wrt.moe/uboot/mediatek

# 固件简要说明

固件每天早上5点自动编译。

固件信息里的时间为编译开始的时间，方便核对上游源码提交时间。

MEDIATEK系列、QUALCOMMAX系列、ROCKCHIP系列、X86系列。

# 目录简要说明

workflows——自定义CI配置

Scripts——自定义脚本

Config——自定义配置

#
[![Stargazers over time](https://starchart.cc/VIKINGYFY/OpenWRT-CI.svg?variant=adaptive)](https://starchart.cc/VIKINGYFY/OpenWRT-CI)
