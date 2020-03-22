---
layout: "post"
title: "[WIP]portfolio"
date: "2020-03-14 15:32"
---

# ETF list
 - VTI
 - VT  : 全球股市
 - VWO :
 - VGK : 歐洲 ETF
 - VEU : 美國以外全球股市
 - VNQ : 美國 REIT
 - VNQI : 美國以外 REIT
 - REET : 全球
 - BND : 美國債券
 - BNDX : 美國除外全球債券
 - BNDW : 全球債券
## backtests
以每個月投3000美元，每季再平衡,所使用的工具是以類別為投資工具而不是實際的ETF，但下還是用實際的 ETF 來當作標地，方便閱讀，但跟實際投資結果可能會有一點出入。(1998還沒有 VWO，不要太計較 ...XD)

標地就是依感覺從簡單到復雜分成:
1. VTI50-VEU40-BND5-VNQ5
模擬股債 9 : 1, 股以美股及美股以外全市場組成，這邊作跟1的對照組，是比較接近真實購買全世界股票。此外導入RETS把不動產想像成債券。
![VTI50-VEU40-BND5-VNQ5]({{ site.baseurl }}/images/2020/03/VTI50-VEU40-BND5-VNQ5.png)

2. VTI50-VWO40-BND5-VNQ5
模擬股債 9 : 1, 股以美股及新興市場組成，這邊想假設歐股跟美股的連動性很高不用分開投入。
![VTI50-VWO40-BND5-VNQ5]({{ site.baseurl }}/images/2020/03/VTI50-VWO40-BND5-VNQ5.png)

3. VTI30-VWO30-VGK30-BND5-VNQ5
模擬股債 9 : 1, 股以美股,歐股及新興市場組成，試看會不會讓再平衡的效果更好。
![VTI30-VWO30-VGK30-BND5-VNQ5]({{ site.baseurl }}/images/2020/03/VTI30-VWO30-VGK30-BND5-VNQ5.png)

依全球的幾個重大金融事件，這裡來假設幾個段資區段，分成投資年限跟投資區間。
![1998-2020-finance-events]({{ site.baseurl }}/images/2020/03/mm-chart_text.png)

---
#### 投資5年 : 1998 ~ 2003 (低點開始定期定額劇情)

從亞洲金融危機低點入市, 經過2000年網路泡沬，SARS一開始就賣出，符合一般想像最完美的投入時機點，這樣會如何呢?

以美股為比較標準
![1998-2003]({{ site.baseurl }}/images/2020/03/1998-2003.png)

[以新興市場為比較標準](https://bit.ly/2WuLS6S)(跟上面有一點修改，但差別不大，懶得重抓了)
![1998-2003_bench_emerging]({{ site.baseurl }}/images/2020/03/1998-2003_bench_emerging.png)

![1998-2003-returns]({{ site.baseurl }}/images/2020/03/1998-2003-returns.png)

結果看來都好過於美國500指數，績效最好的是 VTI50-VWO30-BNDX10 and VTI30-VWO30-VGK30-BNDX5-VNQI5
推測是 VTI50-VWO30-BNDX20 提高了新興市場比例，剛好吃到亞洲金融危機低點入市的便宜。最差跟最好的復合年均成長率(CAGR)差%4，跟美股差則是差9%。

VTI30-VWO30-VGK30-BNDX5-VNQI5 則是一直跟很緊，應該是因為兩者 VWO 的比例一樣而**新興市場是這5年的關鍵**。

---
#### 投資10年 : 1998 ~ 2008 (低點開始定期定額劇情)

從亞洲金融危機低點入市, 經過網路泡沬，SARS，都不賣到2008-12金融海嘨剛開始的時後要用錢的話這樣會如何呢?

以新興市場為比較標準:
![1998-2008]({{ site.baseurl }}/images/2020/03/1998-2008.png)

![1998-2008-return]({{ site.baseurl }}/images/2020/03/1998-2008-return.png)

結果看來都好過於美國500指數，績效最好的是 VTI50-VWO30-BND10 and VTI30-VWO30-VGK30-BND5-VNQI5

最差跟最好的復合年均成長率(CAGR)差%2，跟新興市場指數差則是差6%。最差的VTI50-VEU40-BND5-VNQ5 MWRR變負的，也就是比放銀行還差。最好的 MRR 2.08%差不多就是定存了。

**新興市場是這10年的關鍵**

---
#### 投資5年 : 2008 ~ 2013 (高點開始定期定額劇情)
如果我在2008金融海嘨前當時最高點開始定期投入，一路向下經過歐債危機都堅持投入五年之後走完整個U型谷會怎麼樣呢?

[以美股為比較標準](https://bit.ly/2J5cVxN)
![2008-2013]({{ site.baseurl }}/images/2020/03/2008-2013.png)

以新興市場為比較標準.
![2008-2013_bench-emerging]({{ site.baseurl }}/images/2020/03/2008-2013_bench-emerging.png)

![2008-2013_returns]({{ site.baseurl }}/images/2020/03/2008-2013_returns.png)

這次以VTI50-VEU40-BND5-VNQ5績效最好，VTI50-VWO40-BND5-VNQ5 及 VTI30-VWO30-VGK30-BND5-VNQ5最差，最差跟最好的復合年均成長率(CAGR)差%2，跟美股差則是差6%。

**這5年的關鍵轉換成美國股市**，所以以 VTI + 跟 美股關聯大的 VEU 達到最好的投資比例。

---
#### 投資10年 : 2008 ~ 2018 (高點開始定期定額劇情)
如果我在2008金融海嘨前當時最高點開始定期投入，一路向下經過歐債危機都堅持投入10年會怎麼樣呢?

以美股為比較標準:
![2008-2018]({{ site.baseurl }}/images/2020/03/2008-2018.png)

![2008-2018-return]({{ site.baseurl }}/images/2020/03/2008-2018-return.png)

大致上跟5年的投資期間差不多，因為設定的結束時間為 2018-12，剛好是中美貿易戰，在這個 case 之下，復合年均成長率(CAGR)比起5年的投資少了一半。就當成一個低點需要用錢的case吧。

最差跟最好的復合年均成長率(CAGR)差%2，跟美股差則是差5%。

**這10年的關鍵還是美國股市**。

------

# Obsoleted
 -
![back test with total stocks](images/2020/03/screencapture-portfoliovisualizer-backtest-asset-class-allocation-2020-03-14-21_22_24.png)
---
# reference
 - backtest with asset class : https://bit.ly/2ITK52Z
   - from https://www.portfoliovisualizer.com/
 - https://www.usastock88.com/2012/01/2011.html?m=1
   - https://www.usastock88.com/2009/09/asset-correlations.html
   - https://unicornbay.com/tools/asset-correlations
- https://medium.com/%E6%87%B6%E4%BA%BA%E7%B6%93%E6%BF%9F%E5%AD%B8/etf%E8%B2%B7%E4%B8%8B%E5%85%A8%E4%B8%96%E7%95%8C-%E7%B2%BE%E9%81%B84%E6%94%AF%E5%85%A7%E5%BB%BA-%E6%8A%97%E9%A2%A8%E9%9A%AA-%E8%B3%87%E7%94%A2%E9%85%8D%E7%BD%AE-%E7%9A%84%E9%85%8D%E6%81%AFetf-%E6%9C%80%E9%AB%98%E5%B9%B4%E5%8C%9610-6-%E8%A9%B3%E7%B4%B0%E5%88%86%E6%9E%90aoa-aor-aom-aok%E5%84%AA%E7%BC%BA%E9%BB%9E-5140f5d62737
  - http://katono5566.blogspot.com/2019/08/aoaishares-core-aggressive-allocation.html

# used tools
 - backtest with real etfs : https://www.etfreplay.com/combine.aspx
 - 財經事件時間軸: https://www.macromicro.me/time_line?id=17&stat=2
 - 我的全球金融儀表板 : https://stock-ai.com/myPlotView-GnsqUShk-d
