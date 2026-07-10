# chatgpt-plus-pro-china-guide 发布与收录操作指南

本文件用于把已经完成的本地仓库发布到：

- GitHub 仓库：`https://github.com/he20000405-pixel/chatgpt-plus-pro-china-guide`
- GitHub Pages：`https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/`

当前本地目录：

```text
C:\Users\37132\Desktop\总chonggrok\chatgpt\chatgpt-plus-pro-china-guide
```

以下步骤按顺序完成即可。首次操作不要跳步。

## 第一阶段：在 GitHub 创建空仓库

1. 登录 GitHub 新账号 `he20000405-pixel`。
2. 打开 <https://github.com/new>。
3. `Owner` 选择 `he20000405-pixel`。
4. `Repository name` 填写：`chatgpt-plus-pro-china-guide`。
5. `Description` 填写：

   ```text
   ChatGPT Plus / Pro 国内充值、卡密核销、支付宝微信付款与常见报错指南 | chonggrok.com
   ```

6. 选择 `Public`。GitHub Free 使用分支发布 Pages 时，公开仓库最直接。
7. 不勾选 `Add a README file`。
8. `.gitignore` 和 License 都保持 `None`，因为本地已有文件。
9. 点击 `Create repository`。

完成后先停在 GitHub 给出的空仓库页面，不要在线新建 README。

## 第二阶段：把本地文件提交并推送

打开 PowerShell，把下面命令逐条执行。每执行一条，确认没有红色错误再继续。

### 1. 进入本地仓库

```powershell
Set-Location 'C:\Users\37132\Desktop\总chonggrok\chatgpt\chatgpt-plus-pro-china-guide'
```

### 2. 检查当前分支和文件

```powershell
git status
```

应能看到分支为 `main`，并显示尚未跟踪的文件。

### 3. 连接远程仓库

```powershell
git remote add origin https://github.com/he20000405-pixel/chatgpt-plus-pro-china-guide.git
```

检查地址：

```powershell
git remote -v
```

显示的 fetch 和 push 地址都必须是：

```text
https://github.com/he20000405-pixel/chatgpt-plus-pro-china-guide.git
```

### 4. 暂存文件

```powershell
git add .
```

再次检查：

```powershell
git status
```

确认没有把卡密、session、用户邮箱、订单截图或其他隐私文件加入仓库。

### 5. 创建首次提交

```powershell
git commit -m "Create ChatGPT Plus and Pro China guide"
```

如果 Git 提示没有配置姓名和邮箱，只为当前仓库设置：

```powershell
git config user.name "he20000405-pixel"
git config user.email "你的GitHub邮箱"
git commit -m "Create ChatGPT Plus and Pro China guide"
```

不要把“你的GitHub邮箱”原样执行，应替换成该账号实际邮箱或 GitHub 提供的 noreply 邮箱。

### 6. 推送到 GitHub

```powershell
git push -u origin main
```

如浏览器弹出 GitHub 登录授权，确认登录的是 `he20000405-pixel`，不是旧账号 `usehe`。

## 第三阶段：检查 GitHub 仓库首页

打开：

<https://github.com/he20000405-pixel/chatgpt-plus-pro-china-guide>

检查：

- 首页是否正常显示中文主 README；
- `README_EN.md` 能否打开；
- `guides/` 下是否有 5 篇专题和目录页；
- `_layouts/`、`_includes/`、`assets/` 是否存在；
- README 中的 chonggrok.com 链接是否正确；
- 仓库中是否不存在任何真实卡密、session 和用户数据。

在仓库右侧 `About` 区域点击设置图标：

- Website 填写：`https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/`
- Topics 建议添加：`chatgpt`、`chatgpt-plus`、`chatgpt-pro`、`gpt-5-6`、`china-guide`、`payment-guide`、`chonggrok`

## 第四阶段：开启 GitHub Pages

1. 进入仓库 `Settings`。
2. 左侧找到 `Pages`。
3. 在 `Build and deployment` 下：
   - `Source` 选择 `Deploy from a branch`；
   - `Branch` 选择 `main`；
   - Folder 选择 `/(root)`；
   - 点击 `Save`。
4. 等待 GitHub 完成首次构建。通常需要几分钟，偶尔可能更久。
5. 刷新 Pages 设置页，看到站点地址后打开：

   <https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/>

如构建失败，进入仓库 `Actions`，打开最新的 Pages build 记录查看错误。不要反复修改无关文件。

## 第五阶段：逐页验收

依次打开：

1. <https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/>
2. <https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/>
3. <https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-plus-auto-recharge/>
4. <https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-pro-100-200/>
5. <https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-plus-vs-pro/>
6. <https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/chatgpt-payment-errors/>
7. <https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/guides/gpt-5-6-update/>
8. <https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/en/>
9. <https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/sitemap.xml>
10. <https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/robots.txt>
11. <https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/llms.txt>

桌面和手机各检查一次：导航不重叠、表格可以横向滚动、按钮文字不溢出、所有主站链接都指向 `chonggrok.com`。

## 第六阶段：提交 Google Search Console

1. 打开 <https://search.google.com/search-console>。
2. 新增 `网址前缀` 属性：

   ```text
   https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/
   ```

3. 选择 HTML 标记验证方式，复制 `content` 中的验证码。
4. 打开本地 `_config.yml`，取消下面这行的注释并填入验证码：

   ```yaml
   google_site_verification: "实际验证码"
   ```

5. 提交、推送并等待 Pages 更新：

   ```powershell
   git add _config.yml
   git commit -m "Add Google site verification"
   git push
   ```

6. 回到 Search Console 点击验证。
7. 在 `站点地图` 中提交：

   ```text
   sitemap.xml
   ```

8. 使用 URL 检查，依次请求首页和 5 篇核心专题编入索引。不要同一天无意义重复提交同一 URL。

## 第七阶段：提交 Bing Webmaster Tools

1. 打开 <https://www.bing.com/webmasters/>。
2. 可以从 Google Search Console 导入已验证站点，或手动添加 Pages 地址。
3. 手动验证时，把 Bing 提供的验证码写入 `_config.yml`：

   ```yaml
   bing_site_verification: "实际验证码"
   ```

4. 提交并推送配置更新。
5. 提交站点地图：

   ```text
   https://he20000405-pixel.github.io/chatgpt-plus-pro-china-guide/sitemap.xml
   ```

6. 使用 URL Submission 提交首页和 5 篇核心专题。

## 第八阶段：让主站与 GitHub 形成合理关联

GitHub 已经通过正文链接到以下主站页面：

- `https://chonggrok.com/chatgpt`
- `https://chonggrok.com/verify`
- `https://chonggrok.com/blog/chatgpt-taocan-free-go-plus-pro-2026`
- `https://chonggrok.com/blog/chatgpt-plus-upgrade-guide`
- `https://chonggrok.com/blog/chatgpt-plus-payment-declined-2026`

主站后续可以在对应 Blog 的“延伸阅读”中自然加入一次 GitHub Pages 专题链接。不要在每篇文章底部堆一排重复链接，也不要复制 GitHub 全文回主站。

## 第九阶段：后续更新规则

- 主 README：长期维护流程、业务边界和专题导航；
- GPT-5.6：只在对应专题更新，不反复改主仓库标题；
- 新报错：每个高意向错误单独新增一篇 `guides/*.md`；
- 人民币价格：始终链接主站实时页面，不固定写入文章；
- 官方功能和模型：更新前先核对 OpenAI 官方资料；
- 图片：只加入真实、清晰、已遮盖隐私的截图；
- session：不在公开文章增加详细提取教程；
- 每次修改后检查 `sitemap.xml`、内链和主站链接。

## 常用更新命令

以后修改文章后，在仓库目录执行：

```powershell
git status
git add .
git commit -m "Update ChatGPT guide"
git push
```

推送后等待 GitHub Pages 重新构建，再检查实际网页。
