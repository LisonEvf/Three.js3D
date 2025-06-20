🌱 基于 Three.js + Vue3 + TypeScript + Element-Plus 开发的 3D 模型可视化编辑系统。

---

📦 **分支介绍**

该项目使用模块化设计，主要分为以下几个功能模块：

- **模型编辑**：支持模型加载、材质编辑、动画控制、灯光设置等。
- **场景配置**：提供背景设置、环境贴图、后期效果等功能。
- **交互操作**：支持拖拽、缩放、旋转等交互方式。
- **VR 预览**：提供 VR 场景渲染和交互支持。
- **可视化界面**：基于 Vue3 和 Element-Plus 构建的可视化编辑面板。

---

🌐 **安装 / 启动 / 打包**

请参考 `package.json` 文件中的脚本命令进行安装、启动和打包操作。

```bash
# 安装依赖
npm install

# 启动开发服务器
npm run dev

# 构建生产环境包
npm run build
```

---

🎨 **预览**

项目包含以下主要页面：

- `modelEdit/index.vue`: 模型编辑界面
- `modelPreview/index.vue`: 模型预览界面
- `vrPage/index.vue`: VR 场景预览界面

---

🎵 **主要技术栈**

- **Three.js**：用于 3D 渲染和模型处理
- **Vue3 + TypeScript**：前端框架和类型系统
- **Element-Plus**：UI 组件库
- **IndexedDB**：本地数据存储
- **Draco 压缩**：用于 GLTF/GLB 模型压缩与解压

---

🌺 **开发环境**

- Node.js >= 16.x
- npm 或 yarn
- 支持现代浏览器（Chrome、Firefox、Edge）

---

🍻 **问题 / 功能**

如需提交问题或建议，请前往项目的 Issues 页面。欢迎提交 Pull Request！

---

🗃️ **功能模块介绍**

- **模型加载与渲染**：支持 GLTF/GLB 格式模型加载，支持 Draco 压缩。
- **材质编辑**：支持动态修改模型材质、贴图、颜色等属性。
- **动画控制**：支持播放、暂停、循环动画，支持自定义动画参数。
- **灯光设置**：支持环境光、点光源、聚光灯等光源配置。
- **后期效果**：支持 Bloom、Outline 等后期渲染效果。
- **标签系统**：支持在 3D 场景中添加交互式标签。
- **VR 支持**：提供 VR 场景渲染和交互支持。

---

💥 **注意**

- 使用 Draco 压缩模型时，请确保 `draco_decoder.wasm` 和相关 JS 文件路径正确。
- 模型资源较大时，请优化加载策略以提升性能。
- 使用 IndexedDB 存储数据时，请确保浏览器支持该特性。

---

💚 如果你觉得该项目对你有帮助，请给一个 Star ⭐！

---

🥰 或者请作者喝杯咖啡吧，这将是我持续更新的动力！

联系方式：vx: answer_2027

---

👷 **界面截图**

项目包含多个可视化编辑界面，具体可参考 `src/assets/image/` 中的截图。

---

🍻 **相关链接**

- [Three.js](https://threejs.org/)
- [Element-Plus](https://element-plus.gitee.io/zh-CN/)
- [模型下载网站](https://sketchfab.com/feed)
- [贴图素材网站](https://polyhaven.com/)
- [图片格式转换网站](https://onlineconvertfree.com/zh/convert/hdr/)