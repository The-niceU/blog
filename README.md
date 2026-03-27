# The-niceU Blog

一个基于 Vue3 + Vite 从零搭建的现代化个人博客，已部署于 GitHub Pages，适配多端、支持主题切换、内置完整的文章管理与评论系统。

## ✨ 项目特性
- 🎨 **多主题与暗黑模式**：内置多套主题色，支持亮/暗黑模式一键切换，全局样式无缝适配
- 📱 **全响应式设计**：完美适配桌面端、平板、手机端，针对移动端做了专属交互优化
- 📖 **智能文章目录**：桌面端固定侧边目录栏，移动端抽屉式悬浮目录，滚动自动高亮当前章节
- 💬 **Gitalk 评论系统**：基于 GitHub Issues 实现的评论功能，支持 Markdown 语法、用户登录与回复
- 🏷️ **分类与标签体系**：完整的文章分类、标签筛选功能，快速定位目标内容
- ⬆️ **便捷交互优化**：回到顶部按钮、平滑滚动、文章上下篇导航、hover动效等细节体验优化
- 🚀 **静态部署**：一键构建静态资源，无缝部署到 GitHub Pages，访问速度快、零服务器成本
- 📝 **Markdown 友好**：完整支持 Markdown 语法、代码高亮、表格、列表等技术写作常用格式

## 🛠️ 技术栈
| 技术/工具 | 说明 |
|-----------|------|
| Vue 3 | 前端框架（Composition API 开发模式） |
| Vite | 项目构建工具，开发热更新、生产打包 |
| Vue Router | 单页应用路由管理 |
| MarkdownIt | Markdown 内容解析渲染 |
| Highlight.js | 文章代码块语法高亮 |
| Gitalk | 基于 GitHub 的评论系统 |
| GitHub Pages | 静态页面部署平台 |

## 🚀 快速开始

### 环境要求
- Node.js >= 22.15.1
- npm >= 10.9.2

### 本地运行
1. 克隆项目
```bash
git clone https://github.com/The-niceU/blog.git
cd blog
```
2.安装依赖
`bash
npm install
`

3.启动开发服务器
```bash
npm run dev
```
4.访问项目
打开浏览器访问 ``` http://localhost:5173 ```

### 构建部署
1.构建生产版本
`bash
npm run build
`
2.预览构建结果
`bash
npm run preview
`
3.部署到 GitHub Pages
```bash
# 将构建后的 dist 文件夹内容推送到 gh-pages 分支
# 或者使用 GitHub Actions 自动部署
```
## 📁 项目结构
```plaintext
blog/
├── public/              # 静态资源
├── src/
│   ├── components/      # 公共组件
│   ├── views/           # 页面组件
│   ├── data/            # 文章数据
│   ├── style/           # 全局样式
│   ├── App.vue          # 根组件
│   └── main.js          # 入口文件
├── .gitignore
├── index.html
├── package.json
├── vite.config.js
└── README.md
```

## 🎨 主题配置
项目支持多种主题切换，你可以在``` src/style/global.css ```中自定义主题颜色：
```css
:root {
  --primary: #4c84ff; /* 蓝色主题 */
}

html.theme-purple {
  --primary: #9d65ff; /* 紫色主题 */
}

/* 更多主题... */
```
## 💬 Gitalk 配置
1.在 GitHub 上创建一个新的 OAuth App
2.在 ```src/views/Post.vue``` 中配置 Gitalk：
```javascript
const gitalk = new Gitalk({
  clientID: '你的ClientID',
  clientSecret: '你的ClientSecret',
  repo: '你的仓库名',
  owner: '你的GitHub用户名',
  admin: ['你的GitHub用户名'],
  id: route.params.id,
})
```
## 📝 文章管理
文章数据存储在``` src/data/posts.js ```中，格式如下：
```javascript
export const posts = [
  {
    id: 1,
    title: '文章标题',
    date: '2026-03-27',
    category: '前端',
    tags: ['Vue3', 'Vite'],
    content: `# 文章内容\n\n这里是 Markdown 格式的文章内容...`,
  },
]
```
## 🤝 贡献
欢迎提交 Issue 和 Pull Request！  
1.Fork 本仓库  
2.创建你的特性分支 (`git checkout -b feature/AmazingFeature`)  
3.提交你的更改 (`git commit -m 'Add some AmazingFeature'`)  
4.推送到分支 (`git push origin feature/AmazingFeature`)  
5.开启一个 Pull Request

## 📄许可证
本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 🙏 致谢
- [Vue.js](https://vuejs.org/)
- [Vite](https://vitejs.dev/)
- [Gitalk](https://github.com/gitalk/gitalk)
- 所有为本项目做出贡献的开发者

## 📞 联系方式
- GitHub: <a href="https://github.com/The-niceU" target="_blank">@The-niceU</a>
- 博客: [https://the-niceu.github.io/blog/](https://the-niceu.github.io/blog/)



[![博客首页预览](images/blog-home.png)](https://the-niceu.github.io/blog/)


