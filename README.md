# 灰常小站

基于 [Hexo](https://hexo.io/) + [Fluid](https://github.com/fluid-dev/hexo-theme-fluid) 主题的个人博客，托管于 GitHub Pages，自定义域名 [littlegray.cn](https://littlegray.cn)。

## 仓库结构

- 本分支（`main`）：Hexo 源码
- `gh-pages` 分支：构建产物（由 GitHub Actions 自动生成，**请勿手动修改**）

## 写新文章

### 方式一：本地写作

在 `source/_posts/` 下新建 `.md` 文件（复制现有文章的 front-matter 格式），然后：

``` bash
git add . && git commit -m "post: 新文章标题" && git push
```

### 方式二：GitHub 网页写作

直接在 GitHub 网页上打开 `source/_posts` 目录，新建或编辑文件，提交后自动部署。

push 到 `main` 后，[GitHub Actions](../../actions) 会自动执行 `hexo generate`，并把构建结果发布到 `gh-pages` 分支，约 1 分钟后生效。

## 本地开发

``` bash
npm install       # 安装依赖
npx hexo server   # 本地预览 http://localhost:4000
npm run build     # 生成静态文件到 public/
```

## 站点配置

| 文件 | 作用 |
| ---- | ---- |
| `_config.yml` | Hexo 站点配置（标题、作者、URL 等） |
| `_config.fluid.yml` | Fluid 主题配置（导航栏、首页、关于页、友链等） |
| `source/_posts/` | 文章 |
| `source/img/` | 图片资源（banner、头像、favicon） |

主题配置的完整说明见 [Fluid 官方文档](https://hexo.fluid-dev.com/docs/guide/)。
