# 天玄卡媒体资源库

天玄大陆角色卡所用的全部远端媒体，统一通过 **jsDelivr 全球加速**分发。

## 目录结构

| 路径 | 内容 | 规格 |
|---|---|---|
| `full/` | 角色立绘（细节抽屉） | 768×960 webp ×120 |
| `thumb/` | 角色立绘（图鉴网格） | 256×320 webp ×120 |
| `media/` | 开屏视频与仙乐 BGM | mp4 1.0 MB / mp3 8.2 MB |

## 引用方式

```
https://cdn.jsdelivr.net/gh/q18718859808-sketch/wdqk-portraits@main/<path>
```

## 卡内源链策略

每项媒体均为**多源容灾**，浏览器按序回退：

- **图片**：jsDelivr → kappa.lol → cs.kappa.lol
- **视频**：jsDelivr → kappa.lol → cs.kappa.lol
- **音频**：jsDelivr → kappa.lol → cs.kappa.lol → kappa.lol

## 可用性实测（Chromium 媒体解码判定）

| 媒体 | readyState | 规格 |
|---|---|---|
| `media/tianxuan_preloader.mp4` | 4 | 960×720 · 10.1s |
| `media/bgm_daozong.mp3` | 4 | 360.0s |
| `full/*.webp` | — | 768×960 |
| `thumb/*.webp` | — | 256×320 |

> 注：媒体可用性只能由**浏览器解码**判定，HTTP 层 `curl 200` 不能证明可播。
