# Changelog

## [1.1.0] - 2026-08-29

### ✨ 新特性
- **布局契约重构**：创建根级 `templates/layout.html`，全站 17 个页面统一改用 `~{layout :: html(...)}` 引用，符合 Halo 2.19+ 根布局约定
- **分类切换改为「下划线 Tab」**：首页 / 资源中心 / 工具箱的分类切换统一为应用商店风格 —— 顶部文字 + 选中项蓝色下划线动画，横向可滚动
- **分类栏吸顶固定**：三处分类/筛选栏 `position: sticky` 吸顶（带背景色），滚动时下方内容独立滑动
- **横滑卡片优化**：首页热文 / 资源推荐卡移动端重新收窄并右侧渐隐，一眼可滑动；滑到底最后一张完整显示
- **全局字号变量**：引入 `--fs-page-title / --fs-section-title / --fs-card-title / --fs-card-desc / --fs-meta / --fs-filter`，统一资源中心、工具箱、首页三处聚合页的标题与字体层级，移动端自动降档
- **Hero 图标统一**：资源中心与工具箱标题的 emoji 图标统一为固定尺寸盒子渲染
- **资源推荐卡恢复阅读量显示**（热度标识）

### 🎨 Apple 化（设计体系）
- 文章详情页 / 资源详情页完成 Apple 化（渐变、毛玻璃、pill、入场动画、spring 交互）
- 弹窗搜索（SearchModal）Apple 化
- 修复按压态 / 焦点圆角 bug
- 全程适配 `prefers-reduced-motion`

### 🐛 修复
- 修复横滑卡「滑动后第一次点击失效」：移除 `setPointerCapture` 与冗余 click 拦截，触屏交给原生滚动，点击可正常跳转
- 修复首页推荐末张卡滑底被裁剪
- bfcache 滚动恢复逻辑：卡片返回恢复位置、Tab 切换回顶部

### 🧹 清理
- 删除未使用的模板 `post_resource.html`、`category_resources.html` 及对应 `theme.yaml` 注册

### 📦 安装
1. 下载 `theme-aiym-v1.1.0.zip`
2. Halo 后台 → 外观 → 主题 → 安装主题 → 上传 zip
3. 启用主题

### 🔗 相关链接
- 主页: https://www.aiym.fun
- 文档: https://github.com/myaiym/theme-aiym#readme
- 反馈: https://github.com/myaiym/theme-aiym/issues