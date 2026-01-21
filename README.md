# 🏎️ LMU Pitwall Hub | 模拟赛车指挥台

专为 Le Mans Ultimate (LMU) 玩家打造的个人化赛车指挥台（Pitwall）。这是一个极简、高效、科技感十足的数据中心，旨在帮助车手集中管理分散的赛车数据、工具和笔记。

---

## ✨ 核心功能 (Features)

### 📊 数据速查 (Data Index)
* **快速索引**：一键访问本地 HTML 数据文件（如燃油计算表、圈速数据库、遥测分析报告）。
* **状态管理**：支持 `OPEN` / `ARCHIVE` 状态标签管理。

### 🛠️ 维修区工具箱 (Pitlane Toolkit)
* **常用工具整合**：分类整理外部网站（Popometer, LFM, WEC 官网, Setup Shop）。
* **大按钮设计**：专为比赛间隙优化，方便快速点击。

### 📝 赛道笔记 (Track Notes)
* **专属备忘录**：针对不同赛道记录刹车点、省油策略和车辆设置提示。

### 📒 复盘日志 (Debrief Log)
* **心得记录**：记录排位赛、正赛的复盘心得。
* **版本追踪**：追踪车辆调校变更记录以及版本更新体验。

---

## 🎨 设计风格 (Design)

* **赛车工程风**：采用深黑背景 (`#050505`) 减少屏幕眩光，搭配 **高亮金** (警示/重点) 和 **赛道蓝** (数据/链接)，致敬真实赛车遥测软件。
* **响应式布局**：PC 端采用高效的 2x2 网格视图，移动端自动流式排列。
* **JSON 驱动**：所有内容通过 `json/` 文件夹下的独立文件管理，修改内容无需触碰 HTML 代码。

---

## 🚀 快速开始 (Quick Start)

> ⚠️ **注意**：由于浏览器对本地文件读取的安全限制（CORS 策略），本项目不能直接双击 `index.html` 打开。

### 方法 A：使用 VS Code (推荐)
1.  克隆或下载本项目。
2.  在 VS Code 中打开项目文件夹。
3.  安装插件 **"Live Server"**。
4.  右键点击 `index.html`，选择 **"Open with Live Server"**。

### 方法 B：使用 Python
如果您安装了 Python，可以在项目根目录下运行终端命令：

```bash
python -m http.server 8000

```

然后在浏览器访问 [http://localhost:8000](https://www.google.com/search?q=http://localhost:8000)。

---

## 📂 文件结构

```text
lmu-pitwall/
├── index.html            # 主仪表盘入口
├── race-theme.css        # 核心配色主题变量
├── style.css             # 全局通用样式
├── json/                 # 数据存放区 (在这里修改内容)
│   ├── data_local.json   # 本地文件链接
│   ├── data_tools.json   # 外部工具链接
│   ├── data_tracks.json  # 赛道笔记
│   └── data_logs.json    # 复盘日志
└── data/                 # 您的具体数据页面 (HTML文件)
    ├── fuel_calculator.html
    └── laptimes.html

```

---

## 🛠️ 自定义配置

要修改指挥台显示的内容，只需编辑 `json/` 文件夹下的对应文件：

* **添加新日志**：编辑 `data_logs.json`。
* **新增工具链接**：编辑 `data_tools.json`，支持 `cyan`, `gold`, `white` 三种颜色标记。

---

*Created for Sim Racers, by Sim Racers.*
