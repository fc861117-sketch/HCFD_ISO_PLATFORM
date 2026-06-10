# HCFD ISO Platform

[![GitHub Pages](https://img.shields.io/badge/Deployed-GitHub%20Pages-success.svg)](https://fc861117-sketch.github.io/HCFD_ISO_PLATFORM/)
[![HTML5](https://img.shields.io/badge/Tech-HTML5-orange.svg)]()
[![Jekyll](https://img.shields.io/badge/Jekyll-GitHub%20Pages-blue.svg)]()

新竹縣消防局事故安全官作業平台，整合 ISO 現場作業、事故安全官指引、風險決策、環境氣候監控與化災圖資檢索等功能。

正式平台網址：
[https://fc861117-sketch.github.io/HCFD_ISO_PLATFORM/](https://fc861117-sketch.github.io/HCFD_ISO_PLATFORM/)

## 主要模組

1. **ISO 作業平台**
   - 建立與管理事故安全官作業紀錄。
   - 支援 Briefing、MEDIC、SPE/VTS、風險評估、現場照片與匯出紀錄。

2. **事故安全官作業指南**
   - 提供 ISO 現場作業流程、檢核表與作業提示。
   - 適合現場快速查閱與訓練使用。

3. **風險決策模型**
   - 提供風險矩陣與決策輔助資訊。
   - 協助判斷現場危害、暴露與控制策略。

4. **環境氣候監控及 NOAA**
   - 整合環境與氣候資訊查詢。
   - 輔助掌握風向、天候與現場安全條件。

5. **化災圖資檢索 HAZMAT**
   - 已更新為 `hazmatof400` 版本內容。
   - 包含新版 `database.js`、危害辨識頁面與危害分類圖示。
   - 頁面已接回平台共用導覽列，可從選單返回主平台。

## 專案結構

```text
HCFD_ISO_PLATFORM/
├── index.html
├── _config.yml
├── _includes/
│   └── nav.html
├── Hazmat/
│   ├── index.html
│   ├── database.js
│   ├── README.md
│   └── img/
├── ISO guide/
├── 環境氣候監控及NOAA/
└── 風險決策模型/
```

## GitHub Pages 設定

本專案使用 GitHub Pages / Jekyll 處理共用導覽列。

`_config.yml`：

```yml
baseurl: "/HCFD_ISO_PLATFORM"
```

各子頁若需要共用平台標題欄與選單，頁首需包含 Jekyll front matter，並在 `<body>` 開頭加入：

```html
---
---
<!DOCTYPE html>
...
<body>
    {% include nav.html %}
```

## 本機使用

```bash
git clone https://github.com/fc861117-sketch/HCFD_ISO_PLATFORM.git
cd HCFD_ISO_PLATFORM
```

可直接開啟 `index.html` 檢視靜態頁面；若要完整測試 Jekyll include 與 `site.baseurl`，請使用 Jekyll 或 GitHub Pages 環境。

```bash
bundle exec jekyll serve
```

## 最近更新

- 更新 `Hazmat/` 為 `hazmatof400` 版本內容。
- 新增 `Hazmat/README.md`。
- 修正 `Hazmat/index.html`，加入 Jekyll front matter 與 `{% include nav.html %}`。
- 確保化災圖資檢索頁面開啟後仍保留正式平台標題欄與選單。

## 注意事項

本平台供事故安全官作業輔助與訓練參考使用。實際災害現場仍應依主管機關規範、現場指揮官命令、消防機關 SOP、化學品 SDS/ERG 資訊與即時情資進行判斷。

## 維護者

Developed and maintained by `fc861117-sketch`.
