# Salticat 主页

个人主页 · [www.moee.top](https://www.moee.top)

深色毛玻璃 + 月夜远山 + MikuTap 风格互动。纯静态单文件，零依赖。

## ✨ 功能

- **左栏**：头像 / 渐变流光名字（跟随主题色）/ 简介 / 信息
- **GITHUB**：贡献图动态实时拉取（每次访问最新）
- **PLAY**：MikuTap 风格互动
  - 8×4 无缝点击区，支持滑动演奏、280BPM 节拍量化
  - 音源切换：**MIKU**（原版采样）/ **TETO**（对照表对齐音效）/ **MIX**（左右声道齐唱）/ **AUTO**（随机切换）
  - 背景水印 + 毛玻璃主题色联动（Miku 青 / Teto 红粉）
  - BGM 开关（MikuTap 原版乐谱编排）
- **TIMELINE**：自动读取博客「年度总结」分类文章（实时更新，失败回退静态）
- 格言 / 兴趣 / 站点卡片 / 链接

## 🚀 部署

纯静态站点，任意 Web 服务器托管即可：

```bash
tar -xzf homepage-20260830.tar.gz
sudo mv homepage /var/www/homepage   # Nginx/Caddy root 指向该目录
```

### 接入博客时间线（可选）

编辑 `index.html`，搜 `BLOG_BASE`：

```js
var BLOG_BASE = 'https://blog.你的域名';   // 你的博客域名
var TIMELINE_CATEGORY = '年度总结';        // 与 Halo 分类名一致
```

在 Halo 后台把年度总结文章归入「年度总结」分类，主页时间线自动更新（最多 4 条）。

## ✏️ 修改

所有修改指南都写在 `index.html` 头部注释里（文字搜中文关键词、图片替换 background.svg、GitHub 用户名搜 snovvessel）。

## 📁 结构

```
├── index.html       # 主页面（全部代码）
├── background.svg   # 背景图（可替换）
└── sounds/          # 音效资源
    ├── bgm/         # 背景音乐
    ├── main/        # 原版 Miku 采样
    └── teto_final/  # Teto 成品音效
```

## 🙏 致谢

- [Mikutap](https://aidn.jp/mikutap/)（daniwell）— 互动玩法与音效灵感
- [重音テト](https://kasaneteto.jp/)（ツインドリル）— Teto 音源
