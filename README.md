# ueasy-dist

ueasy 客户端的更新分发仓库（只放 APK 与版本清单，不含源码）。

## 文件

- `version.json` — 应用内更新检查读取的清单
- `ueasy.apk` — 最新安装包

## 更新流程

1. 构建新 APK，递增 `AndroidManifest.xml` 的 `versionCode` / `versionName`
2. 把新 APK 覆盖到本仓库 `ueasy.apk`
3. 更新 `version.json` 的三个字段
4. push，客户端下次启动即可检测到
