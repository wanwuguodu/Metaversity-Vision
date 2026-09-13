# Metaversity 界面字体

应用与 Metaversity-Vision 共用阿里巴巴普惠体 3.0 的官方 Web 字体以及 `typography.css` 变量，正文 Regular（400）、标题与按钮 Medium（500）。通过相对路径加载各自站点的原版字库，不依赖用户本机安装字体。

- 官方来源：[阿里巴巴字体官网](https://www.alibabafonts.com/)，下载核对日期：2026-09-13。
- [Regular 原版 WOFF2](https://fonts.alibabadesign.com/AlibabaPuHuiTi-3/AlibabaPuHuiTi-3-55-Regular/AlibabaPuHuiTi-3-55-Regular.woff2)：5,256,740 字节；SHA-256 `1cb8418d80b01ec08cb6f2d64b6244aaaf1bb80dc35491b66ddba16c5e24f444`。
- [Medium 原版 WOFF2](https://fonts.alibabadesign.com/AlibabaPuHuiTi-3/AlibabaPuHuiTi-3-65-Medium/AlibabaPuHuiTi-3-65-Medium.woff2)：5,469,328 字节；SHA-256 `628a0d5be684bae0e7a8e3ad15b7c4f623fd15b3375082624f778326e343467a`。
- 官方网站指向的[完整法律声明](https://www.yuque.com/yiguang-wkqc2/hgpff0/nus9wiinq4aeiegy)同时保存在 [LICENSE.txt](./LICENSE.txt)，保留中英文全部条款。字体未修改、未转换、未子集化，仅作为界面展示资源使用。

升级字体时在两仓库同时更新资源、来源记录与授权；不得把字体按项目其他代码的许可证重新授权。字体合计约 10.7 MB，使用 `font-display: swap` 保持首访内容可读，Regular 预加载，Medium 由页面按需加载。
