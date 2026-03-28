# [Poke 助力：GitBlog 全自动部署流程记录](https://github.com/jassyip/gitblog/issues/2)

## 📖 项目背景

[GitBlog](https://github.com/yihong0618/gitblog) 是由 yihong0618 开发的一个极简博客方案：用 GitHub Issues 写文章，GitHub Actions 自动构建，GitHub Pages 托管发布。整个流程无需服务器，完全依托 GitHub 生态，非常适合开发者作为个人博客使用。

本次部署由 **Poke**（我的 AI 助手）全程协助，帮我处理了配置细节和繁琐步骤，大大降低了上手门槛 🙏

---

## 🛠 部署流程

### 第一步：Fork 仓库

前往 [yihong0618/gitblog](https://github.com/yihong0618/gitblog)，点击右上角 **Fork**，将仓库 fork 到自己的账号下。

### 第二步：配置 `G_T` Secret

在 fork 后的仓库中，进入 **Settings → Secrets and variables → Actions**，新建一个名为 `G_T` 的 Secret，值为你的 GitHub Personal Access Token（需要有 `repo` 权限）。

这一步是让 GitHub Actions 能够以你的身份操作仓库（提交生成的博客文件）。

### 第三步：修改 `main.py` 和 `config.toml`

- **`main.py`**：填入你的 GitHub 用户名和邮箱，确保 Actions 提交时使用正确的身份信息。
- **`config.toml`**：填写博客标题、描述、作者等个性化配置。

### 第四步：启用 GitHub Pages

进入仓库 **Settings → Pages**，在 **Build and deployment** 中将 Source 设置为 **GitHub Actions**，保存即可。

之后每次在 Issues 新建文章，Actions 会自动触发，构建并部署最新内容到 Pages。

---

## ✅ 部署成果

全流程配置完成后，博客即可通过 `https://<你的用户名>.github.io/gitblog/` 访问。整个发布流程完全自动化：

```
写 Issue → Actions 触发 → 博客自动更新 🎉
```

无需手动 push，无需服务器，GitHub 全家桶搞定一切。

---

## 💛 特别感谢

感谢 **Poke** 在整个部署过程中的大力支持！从 fork 仓库、配置 Secrets、到修改配置文件和启用 Pages，每一步 Poke 都提供了精准的指引，让部署过程顺畅了很多。有了 AI 助手的加持，折腾技术也变得更有乐趣了 😄

---

*记录时间：2026-03-18*