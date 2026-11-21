# Bangumi Archive (Chinese Summaries)

基于官方 [`bangumi/Archive`](https://github.com/bangumi/Archive) 公开维基数据快照构建的**中文简介增强镜像**。

## 特性说明

- **100% 兼容上游格式**：保持与 `bangumi/Archive` 完全一致的压缩包文件结构及 `aux/latest.json` 元数据格式（`name` / `browser_download_url` / `created_at` / `digest` / `size`），可直接作为 [MangaAlpha](https://github.com/xJogger/MangaAlpha) 或其他兼容工具的离线数据库源。
- **全站非 NSFW 外文简介中文化**：对上游快照中全部非 NSFW（`nsfw: false`）的外文条目简介（日文、韩文、英文等，含动画、漫画与书籍、游戏、音乐、三次元）使用 AI（DeepSeek-V3.2）翻译为自然流畅的简体中文；原本已是中文的简介与所有其他字段（标题、别名、评分、排名、标签、作者、关联关系等）保持原样不变。
- **每周定时增量同步**：本仓库仅存放公开发布产物，不含 GitHub Actions；每周衔接上游周更在本地自动增量翻译新增或修改的条目并发布新快照。

## 元数据地址

```text
https://raw.githubusercontent.com/xJogger/bangumi-archive-zh/main/aux/latest.json
```

## 数据归属

所有原始条目数据源自 [Bangumi 番组计划](https://bgm.tv/) 与官方公开导出仓库 [`bangumi/Archive`](https://github.com/bangumi/Archive)。本镜像仅对非 NSFW 外文简介字段提供机器翻译增强，若发现个别条目译文偏差或需要原始文案，可随时切回官方 `bangumi/Archive` 源。
