# Yongxuan Wu — Academic website

白底、单页英文个人学术主页，无需 Node.js、安装依赖或构建。网站内容依据本人提供的信息。

## GitHub Pages 免费部署

GitHub Free 可使用公开仓库免费托管 GitHub Pages，使用 github.io 地址无需购买域名。公开仓库中的网站源文件也对外公开。自定义域名若需要另行注册付费。

1. 登录 GitHub，新建 **Public** 仓库，命名为 `Yarayx.github.io`。你的用户名已配置为 Yarayx。
2. 将本文件夹内的 `index.html`、`styles.css`、`assets/` 和 `.nojekyll` 上传到仓库根目录。不要再套一层 `yongxuan-academic-site/` 文件夹。网页上传可能隐藏 `.nojekyll`；也可在 GitHub 的 Add file → Create new file 中创建它。
3. 打开仓库 **Settings → Pages**。
4. 在 **Build and deployment → Source** 选择 **Deploy from a branch**，分支选 **main**，目录选 **/(root)**，点击 **Save**。
5. 等待部署完成，访问 `https://Yarayx.github.io/`。以 Pages 设置页显示的部署网址为准。
6. 后续直接修改仓库文件并提交，网站会自动更新。

若使用其他仓库名，网址通常为 `https://Yarayx.github.io/仓库名/`。本项目使用相对路径，也支持这种方式。

官方文档：
- https://docs.github.com/en/pages/quickstart
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## 维护

- 个人简介、邮箱、研究兴趣、论文及状态：修改 `index.html`。
- 颜色、字体、间距及手机布局：修改 `styles.css`。
- 头像：放在 `assets/`，修改 `index.html` 中 portrait 图片的路径与替代文字即可。原始真人照片不需要上传到公开仓库。
- 两篇 ISR 稿件目前均未发表；状态变化后手动更新。
- 未添加任何未经提供的 DOI、论文链接、个人履历或导师关系。
- “First-year” 和年份需要在后续按实际情况更新。

## 本地预览

可直接在浏览器打开 `index.html`，无需构建。也可在本文件夹内运行 `python3 -m http.server 8000`，再访问 `http://localhost:8000`。预览结束后按 Ctrl+C 停止。

## 可选：通过 Git 上传

仅在准备好的网站文件夹内操作，确保仓库已经创建：

```sh
git init -b main
git add .
git commit -m "Create academic homepage"
git remote add origin https://github.com/Yarayx/Yarayx.github.io.git
git push -u origin main
```

如果仓库已包含文件，应先克隆仓库后复制网站文件，再提交推送，避免覆盖已有内容。不要将账号密码或访问令牌写入网站文件。
