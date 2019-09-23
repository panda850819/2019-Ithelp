# Day 5 - 五分鐘創建屬於自己的密碼貨幣

2017 年至 2018 年吵得轟轟烈烈的 ICO（Initial Coin Offering），那他們募資的虛擬貨幣是如何創造的呢？很困難嗎？你說昨天教的錢包會用得上?! 
那就跟著我們的腳步，一起看下去吧！

![Photo by Aleksi Räisä on Unsplash](https://miro.medium.com/max/9000/0*k9aLeYNJdK11il7Z)

> 若想要部署自己的虛擬貨幣至**主網**上，請點選右上角的 Networks — 選擇 Main Ethereum Network !

![](https://miro.medium.com/max/641/1*YDpXSPGhHbLPnKJWdH_kBQ.png)

`此篇的教學會採用 Ethereum Ropsten Test Network，若順利測試成功再進行部署至主網（Main Ethereum Network）會比較安全且省錢喔！`

## Step 0 必備條件
```必備條件
- MetaMask 錢包 + 足夠的 ETH
- Chrome 或是 可以安裝錢包的瀏覽器

密碼貨幣規格(Crypto Currency Spec)
- 名稱(Name): NkustCoin
- 符號(Symbol): NKC
- 小數點(Decimal Point): 0
- 代幣總數(Token Amount): 1000
```

## Step 1 複製貼上大法
請先將 MetaMask 的 NetWork 切換到 Ropsten Test Network，並且到這裡[領取免費ETH](https://faucet.metamask.io/)。 
複製「[程式碼(Code)](https://gist.github.com/panda850819/4300543031b341b58921aa1b009166ce)然後將這個貼在「[智能合約編輯器(Smart Contract Online Editor)](https://remix.ethereum.org/)」

![Create ERC-20 contract on Remix](https://miro.medium.com/max/1728/1*oyPiabOp5MpLoRU7R8oKVA.gif)

## Step2 修改參數
```
修改三個參數（Modify three parameters）
姓名（Name） / 符號（Symbol） / 小數點（Decimal）
```

![](https://miro.medium.com/max/1728/1*QkvWVu7cNdHw3BL88ZZ5TA.gif)

## Step3 部署合約
```
設定代幣總數到 1000(設定多少取決於自己喔！）,然後部署合約到 Etheruem 測試網路。 
注意：
1000 with decimal of 2 --> 10.00
每一個單位為 0.01 共有 1000 個 --> 10.00
```

![Deploy ERC-20 smart contract on Remix IDE](https://miro.medium.com/max/1728/1*bS-LI2UA8-yiuOhJJhwY-g.gif)

## Step4 加入貨幣
```
1. 複製 Remix 合約地址
2. 打開 Metamask 錢包
3. 新增代幣（Add tokens）中貼上合約地址
我們將會看到剛剛創建的貨幣 :)
```
![](https://miro.medium.com/max/1728/1*eofx9xg3mdJtx3W0oN4Www.gif)

## 小結
在短短的五分鐘內，我們就完成發幣的動作，需要歸功於 ERC-20 標準，這個標準為 ERC-20 tokens 定義了一個通用的規則。

```
Functions 
1. 總供應量(totalSupply)
2. 代幣餘額(balanceOf)
3. 傳送方(transfer)
4. 從哪傳送來(transferFrom)
5. 指定付款方(approve)
6. 檢查token使用者的代幣數量(allowance)兩個事件
```
```
Events
1. 傳送(transfer)
2. 指定付款方並記錄(Approval)
```
讓我們可以快速地使用 Remix 在 Etheruem... 等主網發布自己的虛擬貨幣！
若想從其他地方查看自己的合約或是貨幣狀況，則需要切換網路（Network），請點選下圖紅框來切換網路！
Ethereum 主網：https://etherscan.io/
Ropsten 測試網：https://ropsten.etherscan.io/