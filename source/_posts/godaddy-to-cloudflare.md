---

title: CloudFlare 代管 GoDaddy DNS
categories: 
  - tech
tags:
  - CDN
  - SSL
  - GoDaddy
  - CloudFlare
date: 2017-08-20 15:04:30

---

前一陣子把 GoDaddy 所購買的 Domain 搬到 CloudFlare 代管，主要是看上免費的 CDN 和 SSL，設定上也很方便

## 新增站台 ##

註冊後，點選畫面的右上角「Add Site」來新增站台吧

<!-- more -->

{% asset_img add-site-1.png 新增 Domain %}
{% asset_img add-site-2.png 掃描 Domain 中 %}
{% asset_img add-site-3.png 掃描 Domain 完成 %}

在 CloudFlare 掃描完成後，會複製你現有的設定，方便接下來的作業，確認沒問題以後就可以下一步了

{% asset_img DNS-records.png DNS 結果 %}

方案的部分我選擇免費的，裡面就已含有 SSL 和 CDN 的功能了

{% asset_img choose-plan.png 選擇方案 %}

接下來就是要從 GoDaddy 移轉出來；CloudFlare 會要求將 Nameservers 改成它所給的

{% asset_img change-nameservers.png Nameservers %}

我原本是 GoDaddy，所以要回到 GoDaddy 去改 Nameservers 的設定

{% asset_img godaddy-nameservers.png GoDaddy Nameservers %}

設定都完成後，需要等待一段時間才會生效，可能要數小時甚至是一天

{% asset_img nameservers-pending.png 等待生效 %}

{% asset_img success.png 轉移完成 %}

## SSL ##

到 Crypto 頁面，SSL 預設是 `Flexible SSL`，不需額外設定，所以當連到網站的時候前面的 protocol 可直接用 https，就會拿到綠色小勾勾徽章 (以為你在打電玩喔...暈～)，若是希望可以幫你把網站都導向 https 的話，可藉由 Page Rules 頁面做設定。

## 加速 ##

到 Speed 頁面，可以試試將 Auto Minify 的功能啟用，會幫忙壓縮檔案

## Caching ##

Always Online 顧名思義就是會保持網站在線，CloudFlare 會定期來網站更新確保資料保持最新的，這同時也會增加網站負荷

## CDN ##

在設定 DNS 的頁面中，當橘色的雲出現表示有 CDN，但因為真實的位置會被藏在 CDN 之後，所以像是 FTP、SSH 之類的服務不要開啟 CDN 喔。

