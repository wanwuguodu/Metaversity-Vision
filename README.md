# Metaversity Vision

Metaversity 的统一 UI 设计规范与交互展示，供 APP 设计、前端开发和界面验收共同参照。

**当前版本：v0.6，手机字号与内容密度。** 已与 Metaversity 应用统一阿里巴巴普惠体 3.0、文字层级、必填红星、默认收起的筛选浮层、起止范围交互、紧凑上下导航与手机字号密度；后续所有相关列表沿用本设计。这里展示的是可复用规则与组件，业务数据均为示例，没有连接学校系统。

## 查看效果

- [阅读 UI 设计规范](./Metaversity-统一UI设计规范.md)
- [清北复交移动服务对标与取舍](./docs/高校校园移动服务视觉对标.md)
- 下载仓库后，使用现代浏览器直接打开 `index.html`，即可查看交互展示。
- [在线查看交互展示](https://wanwuguodu.github.io/Metaversity-Vision/)（GitHub Pages）

也可以在仓库目录运行：

```bash
python -m http.server 8000
```

然后在浏览器访问 `http://localhost:8000`。无需安装前端依赖或执行构建。

## 设计方向

- **搜索直达**：顶部只保留紧凑搜索框，搜索功能入口与功能大分类；学校切换位于个人页，业务页不再重复显示演示环境横幅。
- **APP 优先**：底部一级导航为「首页」「个人」。展示网站的侧栏只是规范目录。
- **内容与入口共存**：容器是功能入口的一种形式；支持图文、轮播、列表与滚动内容，不限定首页的排列方式。
- **统一视觉语言**：参考交我办蓝的主色、中性浅灰背景、白色内容卡片与清晰文字层级；颜色按角色使用，语义状态同时配合文字表达。
- **统一交互反馈**：按钮、表单、导航、弹层和数据状态遵循共同规则。
- **核心内容优先**：搜索常驻、筛选默认收起，电脑端锚定浮层、手机端底部浮层，展开不推挤列表；日期范围在一个入口中先选开始、再选结束，最终成对确认。

| 基础规则 | 候选值 |
| --- | --- |
| 页面背景 / 内容表面 | `#F5F6F8` / `#FFFFFF` |
| 主色 / 按下态 | `#016AED` / `#0058C7` |
| 主文字 / 次要文字 | `#1F2329` / `#606875` |
| 字体 | 阿里巴巴普惠体 3.0，Regular 400 / Medium 500 |
| 电脑字号／行高 | 标题 24/32、分区 18/26、正文 16/24、辅助 14/22 |
| 手机字号／行高 | 标题 20/28、分区 16/24、正文及入口 14/20、辅助 13/20 |
| 输入与标注 | 实际输入均为 16/24；紧凑标注均为 12/18 |
| 间距档位 | 4、8、12、16、24、32 |
| 圆角档位 | 6、8、12、20 |
| 触控目标 | Android 48dp / iOS 44pt |
| Web 紧凑筛选 | 普通控件至少 44px；文字按设备档位，实际输入 16/24；短选项并排、窄屏自然换行 |
| 动效时长 | 操作反馈 160ms / 过渡 260ms；支持减少动态效果 |

具体颜色角色、行高、组件状态与使用约束以设计规范为准。

## 展示内容

HTML 包含十组示例：色彩、字体、间距与圆角、按钮与图标、卡片与列表、表单与筛选、图片与轮播、导航、数据状态、弹层与动效。

可实际操作功能与分类搜索、学校切换示例、活动搜索、筛选浮层、条件计数、日期范围中文滚轮与取消回退，以及表单校验、轮播切换、首页与个人切换、详情返回、重试反馈、确认对话框、底部面板和提示消息。大字与减少动态效果开关便于对比体验。视频区域仅展示封面入口，深色模式尚未定稿。

## 文件与维护

```text
.
├── README.md
├── AGENTS.md                   # 维护边界与同步要求
├── Metaversity-统一UI设计规范.md  # 视觉与交互规则
├── index.html                  # 交互展示，内嵌组件样式、脚本及图片
├── assets/fonts/               # 共用字体变量、官方 Web 字体与完整授权
├── docs/development/           # 中文开发与验证日志
├── docs/高校校园移动服务视觉对标.md # 来源、观察与设计取舍
└── .nojekyll                    # 作为静态文件发布
```

更新时同步规范、HTML 与 Metaversity 应用；字体统一引用 `assets/fonts/typography.css`，与应用 `frontend/public/fonts/typography.css` 保持相同内容。字体来源、文件校验值和完整授权见 [字体说明](./assets/fonts/README.md)。新增和修改相关列表按规范 7.1、7.2 复用筛选浮层与时间范围；实际应用使用公共 `FilterBar` 和 `WheelRangePicker`。两份同名规范完全一致，`index.html` 与应用 `docs/ui-design-preview.html` 仅字体资源路径不同；确需扩展时先补充规范。

发布前检查移动端与桌面布局、键盘操作、表单与弹层状态、文档链接，以及示例数据说明。筛选重点核对展开不推挤列表、独立滚动和焦点恢复；范围重点核对自动切换、日期上下限和取消回退。浏览器验证记录见 `docs/development/`，不将浏览器视口模拟等同真实设备验收。

## GitHub Pages 发布

仓库为 **Public**，通过 GitHub Pages 发布。发布来源为 `Deploy from a branch`，分支 `main`，目录 `/(root)`。推送更新到 `main` 后，GitHub 自动重新部署；可在仓库 `Settings → Pages` 和 `Actions` 中查看状态。

站点地址：<https://wanwuguodu.github.io/Metaversity-Vision/>。

个人 GitHub Free 与组织 Free 均支持公开仓库发布 Pages；个人 Pro 和组织 Team 等套餐还支持私有仓库发布。私有仓库与站点访问权限是独立设置，私有仓库发布的 Pages 站点通常仍公开可访问。详见 [GitHub Pages 官方说明](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)。

## 参考与素材

v0.2 主色 #016AED 参考[交我办官方界面规范](https://developer.sjtu.edu.cn/form/standard/pageStyle.html)，配套色值及组件尺寸为本项目候选规则；四校对标记录区分了官方 APP、小程序和社区项目。规范文档附有其他设计参考来源。展示用建筑摄影来自 [Grand Valley State University](https://www.gvsu.edu/pas/gvsu-resources-101.htm) 和 [Syracuse University Libraries](https://library.syracuse.edu/blog/the-libraries-resources-a-staff-and-faculty-benefit/)，仅作设计讨论示例，不代表项目学校；正式产品素材另行提供。第三方图片不因收录于本仓库而获得新的授权。
