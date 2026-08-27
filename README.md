# SHIKOSYN PE · 官方 APK 发布仓

[![License: Proprietary](https://img.shields.io/badge/License-Proprietary-red.svg)](LICENSE)

**唯一官方 Android 应用更新渠道（patient edition）**

本仓库 [`fujiaqi-boop/new-apk`](https://github.com/fujiaqi-boop/new-apk) 仅用于发布 **SHIKOSYN 创面综合疗愈系统 · 患者端（SHIKOSYN PE）** 的安装包与版本清单，**不是**开源源代码仓库。

> ⚠️ **版权声明**  
> 本仓库全部内容（含 APK、`update.json`）版权归 **fujiaqi-boop** 所有。  
> 详见 [LICENSE](LICENSE) — **禁止**未授权转载、镜像、二次打包、反编译或冒用品牌。

---

## 用户如何更新

1. 在 SHIKOSYN PE App 内打开 **设置 → 关于 → 检查更新**
2. App 将读取本仓库根目录的 [`update.json`](update.json) 并比对版本号
3. 若有新版本，将从此仓库 **GitHub Releases** 下载 APK 并引导安装

**请勿**从非官方渠道安装同名 APK，以免遭遇篡改或恶意软件。

---

## 仓库文件说明

| 文件 | 说明 |
|------|------|
| [`update.json`](update.json) | 应用内更新 manifest（`versionCode` / 下载地址 / 更新说明） |
| [`LICENSE`](LICENSE) | 专有软件发布许可（禁止盗用与再分发） |
| **Releases** | 各版本 APK 附件（通过 GitHub Releases 托管） |

---

## 维护者发布流程

```bash
# 1. 更新 android/app/build.gradle.kts 中的 versionCode / versionName
# 2. 构建 APK
# 3. 编辑 update.json
# 4. 创建 GitHub Release（tag 如 v0.10.0）并上传 APK
# 5. 将 update.json 推送到 main 分支
```

`update.json` 示例：

```json
{
  "versionCode": 25,
  "versionName": "0.10.0",
  "apkUrl": "https://github.com/fujiaqi-boop/new-apk/releases/download/v0.10.0/shikosyn-pe-v0.10.0-debug.apk",
  "apkUrlMirrors": [],
  "releaseNotes": "更新说明",
  "minVersionCode": 1
}
```

源码仓 CI 可参考主项目 `.github/workflows/release-apk.yml`（需配置 `RELEASES_REPO_TOKEN`）。

---

## 禁止行为（摘要）

未经书面授权，**不得**：

- 将本仓库 APK 上传至第三方应用商店或网盘批量传播  
- 搭建镜像站冒充官方更新服务器（个人备份除外，且不得公开提供下载）  
- 修改包名、签名或内嵌后重新发布  
- 使用 SHIKOSYN 名称/标识进行商业宣传  

完整条款见 **[LICENSE](LICENSE)**。

---

## 侵权举报

如发现盗链、二次打包或假冒官方版本，请在本仓库提交 [Issue](https://github.com/fujiaqi-boop/new-apk/issues) 说明：

- 侵权链接 / 截图  
- 发现时间与渠道  

我们将通过平台投诉及法律途径维护权益。

---

## 链接

- 发布仓：<https://github.com/fujiaqi-boop/new-apk>  
- Manifest（raw）：<https://raw.githubusercontent.com/fujiaqi-boop/new-apk/main/update.json>  
- Releases：<https://github.com/fujiaqi-boop/new-apk/releases>  

---

**SHIKOSYN PE** · 创面综合疗愈系统 · 患者端  
© 2026 fujiaqi-boop. All Rights Reserved.
