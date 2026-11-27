# 上海地铁次卡助手

纯静态、单文件网页，可直接部署到 GitHub Pages。

## 本地预览
直接双击 `index.html`，或在本目录运行：

```bash
python -m http.server 8000
```

然后打开 http://localhost:8000 。

## GitHub Pages 部署
1. 在 GitHub 新建一个公开仓库，例如 `shanghai-metro-pass`。
2. 上传本目录中的 `index.html`、`.nojekyll` 和 `README.md`。
3. 进入仓库 **Settings > Pages**。
4. 在 **Build and deployment** 中选择 **Deploy from a branch**。
5. Branch 选择 `main`，Folder 选择 `/ (root)`，点击 **Save**。
6. 等待约 1-3 分钟，GitHub 会显示公开网址。

## 当前功能
- 起点/终点按线路和车站选择
- 原计算方式：最少经停站数 × 平均 1.35 km，再套用票价阶梯
- 官方票价查询按钮用于核对
- 35/45/60/90 次卡比较，默认 45 次卡和剩余 45 次
- 月度购买建议，默认单程票价 7 元
- 纯前端，无后端、无数据库、无第三方依赖

## 注意
线路分支和票价临界点可能造成估算误差，最终票价请以页面中的“官方票价查询（核对）”结果为准。

## 2026-11-27 更新
新增第三页“未来30天”：自动读取当前日期，按连续30个自然日、工作日、公共假期、调休与请假评估次卡，并计算预计用完日期。
