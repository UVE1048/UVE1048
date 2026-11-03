### UVE

三维 GIS · 摄影测量 · 遥感影像处理 · 数字孪生

把实景三维生产链路里那些"只能靠商业软件点鼠标"的环节，做成可脚本化、可容器化的开源工具。

---

#### 开源项目

**ObjOrthoRender** — 把带纹理的 OBJ 三维模型批量渲染成带地理参考的 GeoTIFF 正射影像（DOM）。分块渲染绕开显存上限，Docker 镜像内置 Xvfb + Mesa，无显卡服务器也能跑。

`Python` `pyrender` `rasterio` `GDAL` `Docker`

**Footprint-Creater** — 从高分辨率正射影像自动提取建筑物轮廓，输出可入库的 Shapefile。HRNet 分割 + 全局轮廓校验 + 简化/矩形化，附 Flask 控制台与六阶段实时预览。

`Python` `PyTorch` `MMSegmentation` `HRNet` `Flask` `GIS`

**HRNet-Footprint-Trainer** — 在自有正射影像上训练建筑物轮廓分割模型。滑窗切片数据集生成 + NoData 忽略 + HRNet-W48 训练 + 大图重叠滑窗推理。

`Python` `PyTorch` `MMSegmentation` `遥感`

**VideoFusion-Web** — 无人机视频融合投射到三维实景模型的架构与实现要点。Cesium + EarthSDK3，按相机位姿与 FOV 投影到倾斜摄影模型表面。

`Cesium` `EarthSDK3` `Vue 3` `数字孪生`

---

#### 技术方向

| 领域 | 关键词 |
| :--- | :--- |
| 实景三维 | 倾斜摄影 · 3D Tiles · 网格简化 · 正射影像生产 |
| 遥感智能解译 | 语义分割 · 建筑物提取 · 大图推理 · 矢量化后处理 |
| 数字孪生 | 视频融合 · 场景控制 · UE5 / Cesium 双引擎 |
| 工程化 | 命令行工具 · Docker · 批处理流水线 |

---

#### 协作

欢迎在任意仓库提 Issue 讨论。如果某个工具帮你省下了手工时间，点个 Star 是最直接的支持。
