# Zales 抓取工具

[![Bright Data](https://img.shields.io/badge/Powered%20by-Bright%20Data-FF9A00?style=flat-square)](https://www.bright.cn/) [![爬虫工具 API](https://img.shields.io/badge/Scraper%20API-Available-FF9A00?style=flat-square)](https://www.bright.cn/products/web-scraper/zales) [![数据集](https://img.shields.io/badge/Dataset-Available-0066CC?style=flat-square)](https://www.bright.cn/products/datasets/zales) [![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org) [![许可证：MIT](https://img.shields.io/badge/License-MIT-22C55E?style=flat-square)](LICENSE)

[![推广](https://github.com/bright-cn/Awesome-Web-Scraping/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner%20CN.png)](https://www.bright.cn/products/web-scraper/zales)

> **由 [Bright Data](https://www.bright.cn/) 提供支持的 Zales 数据。**

此代码库提供两种大规模访问 Zales 数据的方式：

- **[方法 1：Bright Data Zales 爬虫工具 API](#方法-1bright-data-zales-爬虫工具-api)**（推荐），完全托管的企业级爬虫 API，可自动处理代理、验证码和扩展。
- **[方法 2：Bright Data Zales 数据集](#方法-2bright-data-zales-数据集)**，可随时下载的预采集 Zales 数据集，无需抓取。

## 目录

- [为什么使用 Bright Data 抓取 Zales？](#为什么使用-bright-data-抓取-zales)
- [方法 1：Bright Data Zales 爬虫工具 API](#方法-1bright-data-zales-爬虫工具-api)
  - [开始使用](#开始使用-zales-爬虫工具-api)
  - [1. Zales 数据](#1-zales-数据)
- [方法 2：Bright Data Zales 数据集](#方法-2bright-data-zales-数据集)
- [数据采集方式](#数据采集方式)

## 为什么使用 Bright Data 抓取 Zales？

抓取 Zales 面临以下几项挑战：

- 速率限制：Zales 会监控请求频率，并可能封禁超出限制的 IP。
- 验证码检测：自动访问可能会触发验证码验证。
- 身份验证障碍：部分数据需要登录才能访问，并且平台会检测自动化操作。
- 动态内容加载：使用 JavaScript 渲染的内容难以通过简单的 HTTP 请求抓取。
- IP 封禁：从同一 IP 重复发送请求可能会导致封禁。

Bright Data 的 Zales 爬虫工具 API 可通过以下功能解决这些问题：

- ✅ **内置动态代理**：自动绕过基于 IP 的速率限制
- ✅ **验证码破解**：无需任何额外设置即可应对机器人检测
- ✅ **结构化数据输出**：获取可直接用于分析的整洁 JSON
- ✅ **无需基础设施**：支持任意规模的云托管抓取
- ✅ **99.9% 正常运行时间 SLA**：为关键业务工作流提供可靠的数据采集

## 方法 1：Bright Data Zales 爬虫工具 API

[Bright Data Zales 爬虫工具 API](https://www.bright.cn/products/web-scraper/zales) 是一种完全托管的解决方案，无需设置任何基础设施。

### 开始使用 Zales 爬虫工具 API

1. **注册**一个[免费的 Bright Data 账户](https://www.bright.cn/)
2. **前往** [Zales 爬虫工具 API](https://www.bright.cn/products/web-scraper/zales)
3. 从控制面板**获取 API 令牌**
4. **安装** `requests` 库：`pip install requests`
5. **运行** `zales_scraper_api_codes/` 中的任意脚本

### 1. Zales 数据

从 Zales 采集数据。

#### 输入参数

| 字段 | 类型 | 必填 | 说明 |
|-------|------|----------|-------------|
| `url` | 字符串 | 是 | 要抓取的 Zales 商品 URL |
| `limit` | 整数 | 否 | 返回结果的最大数量 |
| `include_errors` | 布尔值 | 否 | 在响应中包含错误详情 |
| `notify` | URL | 否 | 数据采集完成时用于接收通知的 Webhook URL |
| `format` | 枚举 | 否 | 输出格式：`JSON`、`NDJSON`、`JSON Lines`、`CSV` |

#### 响应示例

```json
{
  "brand": "Zales",
  "category": "Rings",
  "currency": "USD",
  "in_stock": true,
  "metal": "Sterling Silver",
  "name": "Oval Lab-Created Emerald \u0026 1-1/5 ct. t.w. Lab-Grown Diamond Ring",
  "original_price": 999.0,
  "price": 599.0,
  "product_id": "21238573",
  "rating": 4.4,
  "reviews_count": 38,
  "sizes_available": [
    "5",
    "6",
    "7",
    "8",
    "9"
  ],
  "stone": "Lab-Created Emerald",
  "url": "https://www.zales.com/oval-labcreated-emerald-115-ct-tw-labgrown-diamond-ring-sterling-silver-p21238573.html"
}
```

👉 查看[完整 Python 代码](zales_scraper_api_codes/zales_scraper.py)

## 方法 2：Bright Data Zales 数据集

如果你需要无需编写任何抓取代码即可使用的数据，[Bright Data Zales 数据集](https://www.bright.cn/products/datasets/zales)可提供预先采集、定期更新且可立即下载的数据。

**为什么使用数据集而不是 API？**

- 📦 **即时访问**：无需设置、无需代码，也无需等待数据采集
- 🔄 **定期更新**：按照固定计划持续更新最新数据
- 📊 **多种格式**：可下载为 JSON、JSONL 或 CSV
- 🌍 **超大规模**：涵盖所有主要 Zales 类别的数百万条记录
- ✅ **完全合规**：数据来源符合道德规范并已通过法律审查

👉 **[探索 Zales 数据集](https://www.bright.cn/products/datasets/zales)**

## 数据采集方式

| 功能 | Bright Data 爬虫工具 API | Bright Data 数据集 |
|---------|------------------------|---------------------|
| 所需设置 | 仅需 API 令牌 | 无 |
| 实时数据 | ✅ 是 | ❌ 预先采集 |
| 自定义查询 | ✅ 完全控制 | ❌ 固定架构 |
| 包含代理 | ✅ 内置动态代理 | N/A |
| 验证码破解 | ✅ 自动 | N/A |
| 规模 | 无限 | 无限 |
| 结构化输出 | ✅ JSON / NDJSON / JSON Lines / CSV | ✅ JSON / JSONL / CSV |
| 支持 | 企业级全天候支持 | 企业级全天候支持 |

---

🔗 **了解更多**：[https://www.bright.cn/products/web-scraper/zales](https://www.bright.cn/products/web-scraper/zales)
