# FFmpegKitNext Android Maven 仓库

本分支发布 Fox 使用的预编译库，源码及构建脚本见同仓库 main 分支（基于上游 a724ed99583dcfe2af497c794fdd6b24ddd54a4e）。

- Maven 地址：`https://raw.githubusercontent.com/52PJsoso/ffmpeg-kit-next/maven`
- 依赖坐标：`com.arthenica:ffmpeg-kit-next:9.0.0`
- Android 最低 API：24；ABI：arm64-v8a、armeabi-v7a。
- 传递依赖：`com.arthenica:smart-exception-java:0.2.1`，从 Maven Central 解析。
- AAR/POM 保持本地已验证产物原样，附 SHA-256、SHA-1、MD5 校验文件；已发布版本不可覆盖。
- FFmpeg 实际配置保存在 build-config；启用 LAME、iconv，未启用 GPL 或 nonfree 配置。
- 授权材料见 LICENSE 和 licenses；本次本地源码快照见 sources（含本地补丁，排除 .git 与编译目标文件），基线提交与校验摘要见 sources/manifest.json；构建脚本见 main 分支。

## Gradle 配置

```kotlin
maven {
    url = uri("https://raw.githubusercontent.com/52PJsoso/ffmpeg-kit-next/maven")
    content {
        includeModule("com.arthenica", "ffmpeg-kit-next")
    }
}
```
