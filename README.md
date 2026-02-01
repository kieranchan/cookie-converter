# Cookie Converter

一个用于在多种 Cookie 格式之间转换的纯前端工具，支持表格、JSON、Netscape cookies.txt 的解析与导出，并提供字符串、表格、域名分组等视图。

## 在线访问
- https://kieranchan.github.io/cookie-converter/

## 核心功能
- 解析输入：DevTools 表格粘贴、JSON 数组/对象、Netscape cookies.txt
- 输出视图：Cookie 字符串、表格、按域名分组
- 一键导出：JSON、Netscape、cURL
- 实用工具：URL 解码、复制到剪贴板
- 标记提示：Secure、HttpOnly、SameSite、Session/Expires、敏感字段识别

## 使用方式
1. 打开任意模板页面
2. 将 Cookie 数据粘贴到左侧输入区（或拖拽文件）
3. 点击“转换”或使用 Ctrl + Enter
4. 在右侧切换不同输出视图并复制/导出

## 模板说明
- v1-default：默认完整版（历史记录、主题切换、搜索筛选、拖拽导入）
- v2-glass：玻璃拟态风格
- v3-terminal：终端风格（日志与命令行氛围）
- v4-minimal：极简风格（轻量快速）

## 目录结构
- `index.html`：入口页
- `manifest.json`：PWA 配置
- `v1-default/index.html`
- `v2-glass/index.html`
- `v3-terminal/index.html`
- `v4-minimal/index.html`

## 注意事项
- 全部为静态单页，无需构建步骤
- 本地打开即可使用，或部署到任意静态站点
- 不产生任何外部网络请求（除字体资源，若模板中存在）

## 许可
如需授权或商用，请联系作者。
