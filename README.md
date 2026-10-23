# MH250 Extension Store (Suwayomi / Mihon)

把 [255yun.com](https://255yun.com/)（滴滴漫画网 / 原 mh250.com）接到 Suwayomi 的扩展商店。

> **v1.4.4**: 站点已迁移到 `255yun.com` 并更换新版主题。扩展同步适配：
> - baseUrl 改为 `https://255yun.com`
> - 搜索接口 `/8d3` → `/3aa`
> - 详情/章节路径 `/book/` → `/comic/`（旧书架地址自动重写，无需重新添加漫画）
> - 热门 / 最新 / 章节 / 图片选择器全部适配新版页面
>
> 本站点对部分海外机房 IP 有 Cloudflare 拦截；`255yun.com` 实测可直连。

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
2. 安装 / 更新 **MH250** 到 v1.4.4
3. 在 Sources 启用 **MH250**

> 注意：不要只贴 GitHub 仓库主页 HTML 地址；请贴上面的 raw JSON 地址。

## 直接下载 APK

- [apk/tachiyomi-zh.mh250-v1.4.4.apk](apk/tachiyomi-zh.mh250-v1.4.4.apk)

## 使用提示

- 搜索可输入标题或作者名
- 可直接搜 book id，例如 `ee14419c79`（一人之下）
- 旧版书架里的 `/book/...` 链接会自动映射到 `/comic/...`
- 个别章节可能 502，重试即可

## 版本

- package: `eu.kanade.tachiyomi.extension.zh.mh250`
- version: `1.4.4`
- lib: `1.4`
- 签名 SHA-256: `951454ac11eb97e4ca95b44b44d343969e8e7a0291914e460da4386c57377c4f`

> v1.4.4 与 v1.4.3 使用同一签名证书，可直接覆盖更新。
> 从 v1.4.2 及更早版本升级仍需先删除旧版（v1.4.3 起更换过签名）。

## 免责声明

仅供个人学习与自用。请遵守当地法律与目标网站条款。

## Changelog

- **1.4.4**: 适配站点迁移后的 `255yun.com` 与 mccms 新主题；搜索改 `/3aa`；兼容旧 `/book/` 书架链接；无编号话数不再参与缺章检测。
- **1.4.3**: 站点 443 断连，baseUrl 切换为 `http://www.mh250.com`（图片 CDN 仍走 https）；更换签名证书。
- **1.4.2**: fix false “missing chapters” by parsing chapter numbers from titles instead of site URL ids.
