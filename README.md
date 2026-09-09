# Metaversity Vision

Metaversity 的统一 UI 设计规范与交互展示，供 APP 设计、前端开发和界面验收共同参照。

**当前版本：v0.1 讨论版。** 配色、字号、圆角等是候选视觉基线，尚未作为最终设计定稿。这里展示的是可复用规则与组件，业务数据均为示例，没有连接学校系统。

## 查看效果

- [阅读 UI 设计规范](./Metaversity-统一UI设计规范.md)
- 下载仓库后，使用现代浏览器直接打开 `index.html`，即可查看交互展示。
- [在线查看交互展示](https://wanwuguodu.github.io/Metaversity-Vision/)（GitHub Pages）

也可以在仓库目录运行：

```bash
python -m http.server 8000
```

然后在浏览器访问 `http://localhost:8000`。无需安装前端依赖或执行构建。

## 设计方向

- **APP 优先**：底部一级导航为「首页」「个人」。展示网站的侧栏只是规范目录。
- **内容与入口共存**：容器是功能入口的一种形式；支持图文、轮播、列表与滚动内容，不限定首页的排列方式。
- **统一视觉语言**：暖白背景、深绿主色、清晰文字层级；颜色按角色使用，语义状态同时配合文字表达。
- **统一交互反馈**：按钮、表单、导航、弹层和数据状态遵循共同规则。

| 基础规则 | 候选值 |
| --- | --- |
| 页面背景 / 内容表面 | `#F7F8F6` / `#FFFFFF` |
| 主色 / 按下态 | `#1F6655` / `#174F42` |
| 主文字 / 次要文字 | `#1F2724` / `#5F6B65` |
| 字号层级 | 28、22、18、16、14、12；iOS 正文参考 17 |
| 间距档位 | 4、8、12、16、24、32 |
| 圆角档位 | 8、12、20、28 |
| 触控目标 | Android 48dp / iOS 44pt |
| 动效时长 | 操作反馈 160ms / 过渡 260ms；支持减少动态效果 |

具体颜色角色、行高、组件状态与使用约束以设计规范为准。

## 展示内容

HTML 包含十组示例：色彩、字体、间距与圆角、按钮与图标、卡片与列表、表单与筛选、图片与轮播、导航、数据状态、弹层与动效。

可实际操作搜索与筛选、表单校验、轮播切换、首页与个人切换、详情返回、重试反馈、确认对话框、底部面板和提示消息。大字与减少动态效果开关便于对比体验。视频区域仅展示封面入口，深色模式尚未定稿。

## 文件与维护

```text
.
├── README.md
├── Metaversity-统一UI设计规范.md  # 视觉与交互规则
├── index.html                  # 独立交互展示，内嵌样式、脚本及图片
└── .nojekyll                    # 作为静态文件发布
```

更新时先修改规范，再同步 HTML 中对应的 CSS 变量与组件示例，记录版本变化。新增业务模块沿用颜色角色、字号、间距和状态规则；确需扩展时先补充规范。

发布前检查移动端与桌面布局、键盘操作、表单与弹层状态、文档链接，以及示例数据说明。目前已做结构与脚本语法检查，尚未完成真实设备验收。

## GitHub Pages 发布

仓库为 **Public**，通过 GitHub Pages 发布。发布来源为 `Deploy from a branch`，分支 `main`，目录 `/(root)`。推送更新到 `main` 后，GitHub 自动重新部署；可在仓库 `Settings → Pages` 和 `Actions` 中查看状态。

站点地址：<https://wanwuguodu.github.io/Metaversity-Vision/>。

个人 GitHub Free 与组织 Free 均支持公开仓库发布 Pages；个人 Pro 和组织 Team 等套餐还支持私有仓库发布。私有仓库与站点访问权限是独立设置，私有仓库发布的 Pages 站点通常仍公开可访问。详见 [GitHub Pages 官方说明](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)。

## 参考与素材

规范文档附有设计参考来源。展示用建筑摄影来自 [Grand Valley State University](https://www.gvsu.edu/pas/gvsu-resources-101.htm) 和 [Syracuse University Libraries](https://library.syracuse.edu/blog/the-libraries-resources-a-staff-and-faculty-benefit/)，仅作设计讨论示例，不代表项目学校；正式产品素材另行提供。第三方图片不因收录于本仓库而获得新的授权。
