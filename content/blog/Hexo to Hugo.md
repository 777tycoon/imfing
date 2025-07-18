---
date: '2025-03-20T14:40:54+08:00'
draft: false
title: '從Hexo跳到Hugo：靜態網站生成器的明智選擇'
---

在當今快速發展的網路世界中，靜態網站生成器（Static Site Generator, SSG）成為許多技術部落客和開發者的首選。經過多年使用Hexo後，我決定轉向Hugo，這篇文章將分享我的轉換經驗和選擇邏輯。

Hexo的痛點：NPM依賴地獄

Hexo是一個基於Node.js的優秀靜態網站生成器，我使用它建立了我的技術部落格並維護了相當長的時間。然而，隨著時間推移，一些問題開始顯現：

1. NPM更新帶來的噩夢

每次NPM更新後，我都面臨著各種奇怪的錯誤：

依賴包版本不兼容

插件突然失效

node_modules 文件夾膨脹到令人難以置信的大小

安裝新套件時出現的各種衝突

最令人沮喪的是，有時候只是簡單地執行 npm update 後，整個部落格就無法正常生成，需要花費數小時排查問題。

2. 連結更新的困擾

另一個常見問題是連結管理。當我修改文章結構或移動文件時，Hexo並沒有提供一個簡便的方式來確保所有內部連結保持正確。這導致了許多 404 錯誤，對網站的SEO和用戶體驗造成了負面影響。

3. 構建速度漸漸變慢

隨著文章數量增加，Hexo的構建速度也開始下降。每次更新內容後都需要等待相當長的時間才能看到變更。

為什麼選擇Hugo？

1. Go語言的穩定性與速度

正如同它聲稱的這是"The world's fastest framework for building websites"世界最快的網站架構

Hugo是用Go語言開發的，這帶來了顯著的優勢：

單一二進制文件：不再需要處理複雜的依賴關係

驚人的構建速度：即使有數百篇文章，生成也只需幾秒鐘

跨平台兼容性：在Windows、Mac或Linux上都能無縫運行

2. 減少外部依賴

Hugo的一個主要優點是它幾乎沒有外部依賴。安裝Hugo後，你得到的是一個完整的、自包含的工具，不需要擔心NPM生態系統的變化會破壞你的網站。

3. 豐富的模板系統

Hugo提供了強大而靈活的模板系統，使用Go的模板語言。雖然一開始可能需要學習，但它提供了極大的自由度來自定義你的網站。

4. 內置的文件管理功能

Hugo對內容的組織和管理有非常清晰的概念：

內置的分類系統（taxonomies）

強大的內容組織方式

簡單的短代碼（shortcodes）用於複雜內容

5. 即時預覽功能

這是Hugo相較於Hexo的一大優勢。使用 hugo server 運行本地開發環境後，任何修改都能即時反映在瀏覽器中，而無需重啟伺服器。這大大提高了開發效率，讓我可以更專注於內容創作，而不是等待重新載入。

6. 活躍的社區和持續發展

Hugo有一個活躍的社區和持續的開發。新功能定期加入，bug修復迅速，並且有大量的主題和插件可供選擇。

遷移過程

可能是之前創建Hexo的經驗有幫助，Hugo的創建過程比起來順暢許多

原來放在content/blog的md檔會在public裡被創建出來

從Hexo遷移到Hugo並不像聽起來那麼困難。以下是我的遷移步驟：

安裝Hugo：簡單下載二進制文件或使用包管理器

創建新的Hugo站點：hugo new site myblog

選擇並安裝主題：Hugo有眾多優秀主題可選

轉換內容：

Hexo和Hugo都使用Markdown，但Front Matter語法略有不同

使用簡單的腳本轉換Front Matter格式

調整配置：修改 config.toml（或 config.yaml）以符合需求

測試和部署：

使用 hugo server 本地測試，即時預覽變更

然後部署到網絡

結論

經過幾個月的使用，我可以確信轉向Hugo是一個明智的選擇。構建速度的提升、維護的簡化和更少的技術問題讓我能夠專注於創作內容，而不是解決技術問題。

如果你正在為Hexo的NPM依賴問題和連結管理困擾而苦惱，我強烈建議考慮Hugo作為替代方案。它可能需要一些時間來適應，但長期來看，這個投資是值得的。

用Hugo不再擔心每次NPM更新後可能帶來的災難。現在，我可以專注於創造內容，而不是修復不斷出現的技術問題。