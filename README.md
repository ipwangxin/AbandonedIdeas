# 遗缺点子回收站

一个基于 **GitHub Issues + GitHub Pages + GitHub Actions** 的轻量网站，用来收集、展示和复用被遗弃的软件点子。

很多独立开发项目不是因为没有价值才停止，而是因为时间、推广、技术或商业化卡住了。这个仓库把这些“遗缺点子”沉淀下来，让后来者可以接盘、复盘，或者从失败原因里找到下一步机会。

## 核心功能

- 用 GitHub Issue 表单收集遗弃报告
- 自动读取带 `abandoned` 标签的 Issue
- 在 GitHub Pages 上展示点子列表、遗弃原因和作者
- 自动统计热门遗弃原因，支持点击筛选
- 当用户因为“推广困难，找不到用户”而放弃时，引导了解“流量互助联盟”
- 通过 GitHub Actions 定时生成 `docs/data.json`，减少前端 API 限制

## 在线页面

启用 GitHub Pages 后，网站地址通常是：

```text
https://ipwangxin.github.io/AbandonedIdeas/
```

流量互助联盟页面：

```text
https://ipwangxin.github.io/AbandonedIdeas/lianmeng.html
```

## 如何提交一个遗缺点子

1. 打开仓库的 Issues 页面。
2. 点击 **New issue**。
3. 选择 **提交遗缺点子** 表单。
4. 填写点子名称、一句话描述、遗弃原因、技术栈、已做工作等信息。
5. 提交后，Issue 会带上 `abandoned` 标签。
6. GitHub Action 会在触发后生成最新的 `docs/data.json`，首页会展示这条记录。

## 如何启用 GitHub Pages

1. 进入仓库设置：`Settings`。
2. 打开 `Pages`。
3. 在 `Build and deployment` 中选择：
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/docs`
4. 保存后等待 GitHub Pages 部署完成。

## 数据同步方式

工作流文件位于：

```text
.github/workflows/sync-issues.yml
```

它会在以下场景运行：

- 新 Issue 创建、编辑、打标签、关闭或重新打开
- 每小时定时运行一次
- 手动点击 `Run workflow`

同步结果会写入：

```text
docs/data.json
```

首页优先读取这个静态 JSON 文件。如果文件不存在，才会回退到 GitHub API。

## 流量互助联盟

当提交者选择 **“推广困难，找不到用户”** 作为遗弃原因时，Issue 表单底部会展示“流量互助联盟”的提示。

联盟目标很简单：

- 帮早期产品找到第一批用户
- 通过成员之间互挂链接共享流量
- 用人工审核和轻量规则保证质量

联盟介绍页位于：

```text
docs/lianmeng.html
```

你可以手动修改其中的：

- 已加入开发者数量
- 申请入口链接
- Google Form 嵌入地址
- FAQ
- 成员规则

## 运营 SOP

前 10 个用户建议人工运营：

1. 每天查看新提交的 `abandoned` Issue。
2. 对高质量点子补充标签，例如 `推广困难`、`可接盘`、`技术卡点`。
3. 对选择“推广困难，找不到用户”的提交者，手动评论邀请加入流量互助联盟。
4. 把被接盘或复活的点子写进首页“成功案例”区域。
5. 每周检查一次联盟成员链接是否有效。

首页成功案例在这里维护：

```text
docs/index.html
```

搜索 `成功案例` 即可找到对应区块。

## 后续可扩展方向

- 增加联盟申请专用 Issue 模板
- 增加 `members.json` 展示联盟成员
- 给每个遗弃原因增加独立页面
- 根据技术栈、领域、原因做自动匹配
- 统计接盘状态和成功案例

## English

English documentation is available in [README.en.md](README.en.md).
