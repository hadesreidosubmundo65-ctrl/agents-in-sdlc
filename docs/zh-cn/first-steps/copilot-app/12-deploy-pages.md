---
title: "第 12 课 - 使用 GitHub Pages 部署网站"
description: "使用 GitHub Copilot app 配置 Pages 工作流、审查 pull request，并验证 Space Quiz 已成功上线。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

使用 GitHub Pages 部署 Space Quiz，让其他人也能访问。Copilot 可以准备工作流并指导部署，但仍需自行审查更改并确认网站已上线。

在本课中，你将：

- 请 Copilot 配置 GitHub Pages 部署。
- 在合并前审查工作流和 pull request。
- 跟进部署并验证已发布的网站。

## 场景

Space Quiz 已位于 GitHub 仓库中，但其他人还缺少一种简单的体验方式。使用 GitHub Pages 发布这个单文件网站后，其他人就能通过公共 URL 访问，而且无需添加服务器或运行时依赖项。

## 请 Copilot 部署网站

在 `space-quiz` 的 Copilot app 会话中发送以下提示：

```plaintext
为此仓库启用 GitHub Pages。创建一个 GitHub Actions 工作流，在需要时构建网站并将其部署到 GitHub Pages。如果仓库中还没有 README，请添加一个，介绍此应用以及如何在本地运行。使用这些更改创建 pull request，并在必需的检查通过后合并。持续监视部署，直到部署成功，然后报告线上网站的最终 URL。如果你没有权限启用 Pages 或合并 pull request，请明确告诉我需要批准或执行什么操作；在网站上线之前不要报告成功。
```

![三阶段示意图：已合并的 space-quiz pull request；成功运行的 GitHub Actions Deploy website，其中包含 Build website、Upload artifact 和 Deploy to Pages 步骤；以及通过 yourname.github.io/space-quiz/ 访问的在线 Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> 此提示要求代理创建并合并 pull request，以及更改仓库的 Pages 设置。继续前，请审查 diff、部署权限和 GitHub 的任何审批提示。

## 审查工作流并验证部署

1. 确认只有在仓库原本没有 README 时才添加了 README。
2. 审查 pull request 中的更改，包括工作流的构建和部署步骤。
3. 仅在必需的 pull request 检查通过后才合并。
4. 持续跟进 GitHub Actions 部署运行，直到成功。
5. 打开报告的 URL，确认 Space Quiz 可以加载。

如果代理无法启用 Pages 或合并 pull request，请按照它提供的具体说明操作。在部署成功且在线网站能够加载之前，不要将任务视为已完成。

## 总结和后续步骤

Space Quiz 现已作为在线网站提供，并且你亲自验证了部署，而不是只依赖代理的报告。继续学习[第 13 课：回顾与后续步骤][next-lesson]。

[next-lesson]: ../13-review/
