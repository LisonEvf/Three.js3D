

# 🌱 Three.js3D - 3D 模型可视化编辑系统

基于 Three.js + Vue3 + Typescript + Element-Plus 开发的 3D 模型可视化编辑系统，支持模型编辑、VR 预览、材质调整、光照配置等多种功能。

## 📦 分支说明

| 分支 | 说明 |
|------|------|
| `master` | Vue3+Pinia+Javascript，最新功能和问题修复 |
| `ts-master` | Vue3+Pinia+Typescript，master 的 TypeScript 版本 |
| `develop` | Vue3+Pinia+Javascript，开发中功能重构 |
| `gh-pages` | GitPages 线上包分支 |

## 🚀 快速开始

### 环境要求

- Node.js >= 18.0.0
- npm / yarn / pnpm

### 安装依赖

```bash
# 使用 npm
npm install

# 或使用 yarn
yarn install

# 或使用 pnpm
pnpm install
```

### 启动项目

```bash
# 开发模式
npm run serve

# 生产构建
npm run build

# 或使用 yarn/pnpm
yarn serve / yarn build
pnpm serve / pnpm build
```

## 🎨 功能特性

### 核心功能模块

| 模块 | 功能 |
|------|------|
| 背景管理 | 背景图加载、全景图、外部 HDR/图片/视频 |
| 材质编辑 | 材质类型切换、属性修改、贴图调整 |
| 后期处理 | 辉光效果、模型分解、拖拽缩放 |
| 灯光控制 | 环境光、平行光、点光源、聚光灯 |
| 动画系统 | 动画播放、配置修改、轴旋转 |
| 辅助工具 | 坐标轴、网格辅助、位置调整 |
| 3D 标签 | 标签拖拽、内容编辑 |
| 多模型 | 多选、位置旋转、缩放调整 |

### 技术栈

| 技术 | 版本 |
|------|------|
| Vue | 3.5.x |
| Vite | 4.3.x |
| Three.js | 0.169.x |
| Element Plus | 2.4.x |
| Pinia | 2.1.x |
| Axios | 1.5.0 |

## 📁 项目结构

```
├── public/               # 静态资源
│   ├── threeFile/       # Three.js 模型文件
│   └── draco/           # Draco 压缩库
├── src/
│   ├── assets/          # 资源文件
│   ├── components/      # 公共组件
│   ├── config/          # 配置文件
│   ├── layouts/         # 布局组件
│   ├── router/          # 路由配置
│   ├── store/           # Pinia 状态管理
│   ├── style/           # 样式文件
│   ├── utils/           # 工具函数
│   │   ├── modelEditClass/   # 模型编辑模块
│   │   ├── initThreeTemplate.jsx
│   │   └── renderModel.js
│   └── views/           # 视图组件
├── index.html
├── package.json
└── vite.config.js
```

## 📖 使用说明

### 模型加载

- 支持 GLB、GLTF、OBJ、USDZ 等格式
- 支持 Draco 压缩模型
- 部分大模型加载可能需要较长时间

### 数据存储

- 编辑配置存储在 localStorage
- 清除缓存可解决数据相关问题

### 注意事项

- 建议使用 Chrome 浏览器
- 大模型对内存要求较高
- 外部模型不支持预览和保存
- 模型数量过多可能导致浏览器崩溃

## 🔗 相关链接

- [Three.js 官网](https://threejs.org/)
- [Element Plus](https://element-plus.gitee.io/zh-CN/)
- [模型下载](https://sketchfab.com/feed)
- [贴图素材](https://polyhaven.com/)

## 📄 许可证

本项目基于 MIT 许可证开源。

## 💬 反馈与支持

如有问题或功能建议，欢迎提交 [Issues](https://gitee.com/ZHANG_6666/Three.js3D/issues)

---

如果这个项目对您有帮助，欢迎点亮 ⭐ Star 支持作者！