# letianhello.cn

这是一个可直接部署到 GitHub Pages 的个人博客静态站点。

## 目录结构

- `index.html`：首页
- `about.html`：关于页
- `posts/`：文章页
- `styles.css`：统一样式
- `assets/favicon.svg`：站点图标
- `CNAME`：自定义域名配置
- `.nojekyll`：禁用 Jekyll 处理
- `robots.txt` / `sitemap.xml`：基础 SEO 文件

## 部署到 GitHub Pages

1. 在 GitHub 新建一个仓库，例如 `letianhello-blog`。
   建议直接用公开仓库；如果要私有仓库发布 GitHub Pages，需要对应付费计划支持。
2. 把当前目录全部文件上传到仓库根目录。
3. 打开 GitHub 仓库的 `Settings` -> `Pages`。
4. 在 `Build and deployment` 里选择：
   - `Source`: `Deploy from a branch`
   - `Branch`: `main` / `root`
5. 在 `Custom domain` 里填写 `letianhello.cn`。
6. 等待 GitHub Pages 发布完成。

## 绑定域名 letianhello.cn

仓库里已经包含 `CNAME` 文件，内容是：

```txt
letianhello.cn
```

建议先在 GitHub Pages 设置里填好 `letianhello.cn`，再去域名服务商后台配置 DNS。

你还需要在域名服务商后台配置 DNS：

- 主域名 `@`：添加 `A` 记录到 GitHub Pages IP
- `www`：添加 `CNAME` 到你的 GitHub Pages 默认域名

常见 GitHub Pages `A` 记录值：

- `185.199.108.153`
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

`www` 的 `CNAME` 一般指向：

```txt
<你的 GitHub 用户名>.github.io
```

可选但推荐：

- 在 GitHub 账号设置里验证 `letianhello.cn`，避免自定义域名被其他仓库误占用。

## 后续可继续做的升级

- 增加文章列表页和分页
- 接入评论系统（如 Giscus）
- 改成 Jekyll / Astro / Hugo
- 增加 RSS、归档页、标签页
