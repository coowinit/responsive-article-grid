# Responsive Article Grid / 响应式文章卡片网格

一个受技术博客 / Changelog 卡片布局启发的原生 HTML + CSS 演示项目。无需框架、无需 JavaScript、无需联网，直接打开 `index.html` 即可预览。

## 功能

- 桌面 3 列、平板 2 列、手机 1 列（断点：992px / 768px）
- CSS Grid 自动实现**同行等高**，不同网格行可以有不同高度
- Flexbox + `margin-top: auto`：作者信息始终位于卡片底部
- 分类/日期两端对齐，标题和摘要自然换行
- 轻微 Hover 边框和标题颜色变化，键盘焦点样式，减少动画偏好适配
- 12 张英文示例卡片、三张本地 SVG 占位头像，完全离线运行

## 项目结构

```text
responsive-article-grid/
├── index.html
├── assets/
│   ├── css/article-grid.css
│   └── images/avatars/{fede,chris,xavier}.svg
└── README.md
```

## 使用

1. 解压缩后直接在浏览器打开 `index.html`。
2. 在 `index.html` 中复制 `<article class="article-card">...</article>` 增加卡片。
3. 修改 `assets/css/article-grid.css` 的 CSS 变量、间距及媒体查询，即可定制外观。
4. 若集成到 WordPress，动态生成每篇文章的标题、摘要、日期、分类和作者即可；卡片布局 CSS 不依赖 WordPress。

## 注意事项

- 本项目以布局演示为目的，文章标题链接目前使用 `#article-xx` 页面内锚点占位，并**不指向真实文章**。接入网站时请替换为真实文章 URL。
- 示例文案是布局测试内容，部分来自参考截图，部分是模拟数据；不代表实际发布信息。
- 头像是自行绘制的占位 SVG，并非真实作者照片。
- 为适应长度不同的文本，默认不固定卡片高度、不截断标题或摘要。

## 后续扩展方向

可独立添加 WordPress 循环模板、分类筛选、分页或加载更多；建议保持当前原生 CSS 组件的简洁性，不为基础布局引入 JS 依赖。
