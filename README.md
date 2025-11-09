# TV Maze 网络爬虫与数据分析项目

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green.svg)](https://pandas.pydata.org/)
[![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-Web%20Scraping-orange.svg)](https://www.crummy.com/software/BeautifulSoup/)

一个基于 TV Maze 网站数据的电视节目质量分析项目，通过网络爬虫收集 500+ 部电视节目数据，深入探索影响电视节目质量的关键因素。

## 📋 项目简介

本项目从 [TV Maze](https://www.tvmaze.com/) 网站抓取电视节目数据，通过系统性的数据分析，回答一个核心问题：**什么因素决定了电视节目的质量？**

### 研究问题

1. **类型影响**：某些类型是否更容易获得高评分？
2. **时间演变**：电视节目评分如何随年代变化？
3. **网络竞争**：哪些电视台/平台制作出最优质的内容？
4. **时长与质量**：节目持续时间是否与评分相关？

## ✨ 主要功能

- 🔍 **网络爬虫**：使用 `requests` 和 `BeautifulSoup` 从 TV Maze 抓取节目数据
- 🧹 **数据清洗**：处理缺失值、解析类型标签、计算节目时长等
- 📊 **数据分析**：多维度分析类型、年代、网络、时长等因素
- 📈 **数据可视化**：使用 `matplotlib` 和 `seaborn` 生成丰富的图表
- 💾 **数据导出**：将清洗后的数据保存为 CSV 文件

## 🛠️ 技术栈

- **Python 3.x**
- **requests** - HTTP 请求库
- **BeautifulSoup4** - HTML 解析
- **pandas** - 数据处理与分析
- **numpy** - 数值计算
- **matplotlib** - 数据可视化
- **seaborn** - 统计图表

## 📦 安装

### 环境要求

- Python 3.7+

### 依赖安装

```bash
pip install requests beautifulsoup4 pandas numpy matplotlib seaborn
```

## 🚀 使用方法

1. **克隆仓库**
```bash
git clone <repository-url>
cd <repository-name>
```

2. **运行 Jupyter Notebook**
```bash
jupyter notebook data.ipynb
```

3. **执行代码**
   - 按顺序运行所有代码单元
   - 爬虫会自动抓取数据（注意：需要较长时间，请耐心等待）
   - 数据会自动保存为 `data.csv`

## 📊 数据说明

### 数据字段

- **Title**: 节目名称
- **First air date**: 首播日期
- **End date**: 结束日期
- **Rating**: 评分（0-10）
- **Genres**: 类型标签
- **Status**: 状态（Running/Ended）
- **Network**: 播出平台
- **Summary**: 简介

### 数据规模

- **总样本数**: 500 部电视节目
- **时间跨度**: 1960s - 2020s
- **数据来源**: TV Maze 网站

## 🔍 主要发现

### 1. 类型影响分析

- **顶级类型**：Anime (8.07)、War (7.90)、Mystery (7.88)、Crime (7.84)
- **最佳组合**：Drama + Crime 组合通常获得 8.5+ 的高评分
- **关键洞察**：类型组合比单一类型更重要，2-3 个类型的组合是最优选择

### 2. 时间演变趋势

- **黄金年代**：2000s-2010s 是电视质量的巅峰时期
- **质量下降**：2010s 虽然内容数量增加了 2.6 倍，但平均评分下降了 3.4%
- **数量-质量悖论**：内容爆炸式增长导致平均质量被稀释

### 3. 网络平台分析

- **优质平台**：HBO、Showtime、AMC 等付费平台评分最高（8.0+）
- **传统广播**：CBS、NBC、ABC 等传统电视台评分中等（7.0-7.5）
- **流媒体平台**：Netflix、Amazon 等平台评分方差较大

### 4. 时长与质量关系

- **最佳时长**：3-5 年是最优的节目运行时长
- **质量下降**：超过 10 年的节目通常评分较低
- **规划效应**：有明确结局规划的节目表现更好

## 📈 可视化图表

项目包含以下可视化分析：

1. **类型评分分布图** - 展示各类型的平均评分排名
2. **年代趋势图** - 显示评分随年代的变化趋势
3. **网络平台箱线图** - 比较不同平台的评分分布
4. **时长-评分散点图** - 探索时长与质量的关系
5. **类型共现热力图** - 分析类型组合模式
6. **Top 20 节目排名** - 展示评分最高的节目

