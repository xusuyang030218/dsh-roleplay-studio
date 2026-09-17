# 角色扮演工作区第一阶段实施计划

## 1. 建立可回滚基线
- 备份当前运行中的 `C:\Users\23074\.dsh\profiles\web\node_modules\@furongjun1999\dsh-memory\lib\roleplay_web.js`。
- 将运行文件复制到 `dsh-roleplay-studio/runtime/roleplay_web.js`，让个人仓库拥有可审查版本。

## 2. 重构页面壳层
- 在 HTML/CSS 中引入语义化颜色变量、统一间距、面板和按钮样式。
- 增加顶部工作区栏、角色状态区、服务状态提示和清晰的空状态。
- 调整桌面端宽度和移动端布局，避免页面内容被浮动入口遮挡。

## 3. 统一客户端请求和状态
- 增加 `requestJson`：统一超时、HTTP 状态和错误结构解析。
- 增加错误提示条、服务状态提示和可恢复错误文案。
- 改造发送流程：保留草稿、显示 pending、失败后提供重试。
- 改造历史加载：请求序列号/AbortController 防止旧响应覆盖当前角色。
- 改造角色详情保存：检查每一步返回值，失败不关闭弹层。

## 4. 验证
- 用 Node 进行语法检查。
- 检查个人仓库 diff 和运行文件内容一致。
- 在本机 DSH 页面刷新后验证角色列表、历史、发送失败提示和移动端布局。

## 5. 提交
- 将设计文档、计划文档和 runtime 源码提交到 `dsh-roleplay-studio`。
- 推送到 `https://github.com/xusuyang030218/dsh-roleplay-studio`。
