# MH250 Extension Store (Suwayomi / Mihon)

把 [mh250.com](https://www.mh250.com/) 接到 Suwayomi 的扩展商店。

## 在 Suwayomi 添加扩展商店

打开 **扩展 → 扩展商店 / Extension Stores → 添加**，粘贴：

### 推荐（legacy，兼容性最好）

```text
https://raw.githubusercontent.com/cmulittlechild/suwayomi-mh250-extension/repo/index.min.json
```

### 也可

```text
https://raw.githubusercontent.com/cmulittlechild/suwayomi-mh250-extension/repo/repo.json
```

```text
https://raw.githubusercontent.com/cmulittlechild/suwayomi-mh250-extension/repo/index.json
```

添加成功后：
1. 刷新扩展列表
2. 安装 **MH250**
3. 在 Sources 启用 **MH250**

> 注意：不要只贴 GitHub 仓库主页 HTML 地址；请贴上面的 raw JSON 地址。

## 直接下载 APK

- [apk/tachiyomi-zh.mh250-v1.4.2.apk](apk/tachiyomi-zh.mh250-v1.4.2.apk)

## 使用提示

- 搜索可输入标题；不稳定时会回退过滤
- 可直接搜 book id，例如 `ee14419c79`（一人之下）
- 个别章节可能 502，重试即可

## 版本

- package: `eu.kanade.tachiyomi.extension.zh.mh250`
- version: `1.4.2`
- lib: `1.4`

## 免责声明

仅供个人学习与自用。请遵守当地法律与目标网站条款。

## Changelog

- **1.4.2**: fix false “missing chapters” by parsing chapter numbers from titles instead of site URL ids.
