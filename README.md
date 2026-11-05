# 中国收集 · China Collecting

足迹地图。去过的地方可以点亮、备注。

## 怎么用

双击 `China_Collecting.html` 就能用。不需要联网、安装。

- 点一个区域 →「收集」，就会一直亮着。
- 「记录」可以给这个地方写点东西
- 滚轮缩放，双击复位

## 数据存在哪

默认存在浏览器里（localStorage）。换浏览器、清缓存会丢。

推荐点右上角 **「绑定数据文件夹」**，选中 `China_Collecting` 文件夹并授权。
之后每次收集、记录都会自动写进文件夹里的 `footprints.json`，
下次打开自动读回

> 绑定功能用到 File System Access API，需要 Chrome / Edge 等 Chromium 内核浏览器。
> 不支持时会自动退回浏览器存储，功能不受影响，只是数据不落盘。

「导出备份 / 导入恢复」可手动导出 JSON，和 `footprints.json` 是同一种格式，互相通用。

## 目录结构

```
China_Collecting.html   界面与全部逻辑（约 60KB）
data/   地图边界：省级 34 / 地级 389 / 世界 216 国 / 南海九段线
lib/    echarts.min.js  渲染引擎
```

## 数据来源

- 省级 / 地级 行政区划边界（不含台湾县市）：阿里云 DataV.GeoAtlas
- 台湾省 22 个县市边界：taiwan-atlas（数据源自 內政部國土測繪中心「國土測繪圖資服務雲」，TopoJSON 经 topojson-client 转换后并入本地数据）
- 世界 216 国边界、南海九段线：阿里云 DataV.GeoAtlas
- 渲染引擎：Apache ECharts

地图数据与引擎的版权归各自作者所有，请遵守其原始授权条款。
