# Day 08 - 區塊鏈小常識篇 - 加密雜湊傻傻分不清楚

身為一個不正統的資科人，常常聽到外界對加密以及雜湊的見解十分有趣，因此今天就來解決大家對於這兩者的疑惑！

```
目錄
> - 加密
> - 雜湊
> - 小記
> - 資料來源
```
## 加密（ Encryption ）

> 加密是什麼呢？

加密是種用來將資料加以編碼的數學演算法，只有預期的對象可以加以讀取。
這樣講感覺有點太 HardCore ... XD
假如說：國王要把他的遺產鎖在王宮的寶箱裡面，那麼那個「鎖」等同於加密動作，「鑰匙」等同於解密動作。

![https://ithelp.ithome.com.tw/upload/images/20190923/201183251rRyQXU5GB.png](https://ithelp.ithome.com.tw/upload/images/20190923/201183251rRyQXU5GB.png)

那我們通常加密會分成兩種
- 對稱式金鑰加密
如名，加密和解密金鑰是相同的。通訊方必須具有相同的金鑰才能實現安全通訊。
缺點：如果遇到中間人攻擊，那麼所有加密的內容都容易被破解，內容會十分的危險。

- 非對稱式金鑰加密
如名，加密和解密金鑰是不相同的。
下圖，（BP1 = Bob Public Key ， BP2 = Bob Private Key ， AP1 = Alice Public Key ， Alice Private Key ）

> 訊息加密
假設 Alice 要傳送一則訊息給 Bob 卻不想給人看到，那他就可以透過非對稱金鑰加密去達成。
![https://ithelp.ithome.com.tw/upload/images/20190923/20118325Qwdj5njSN3.png](https://ithelp.ithome.com.tw/upload/images/20190923/20118325Qwdj5njSN3.png)
![https://ithelp.ithome.com.tw/upload/images/20190923/20118325Bl0GJmfZah.png](https://ithelp.ithome.com.tw/upload/images/20190923/20118325Bl0GJmfZah.png)

> 數位簽章
假設 Bob 收到一份 Alice 寄來的文件，他要確認這份文件是否是 Alice 寄來的。
![https://ithelp.ithome.com.tw/upload/images/20190924/20118325DMBNr6tECB.png](https://ithelp.ithome.com.tw/upload/images/20190924/20118325DMBNr6tECB.png)
![https://ithelp.ithome.com.tw/upload/images/20190924/20118325Olo1ocRHuZ.png](https://ithelp.ithome.com.tw/upload/images/20190924/20118325Olo1ocRHuZ.png)

## 雜湊（ Hash ）
我們在區塊鏈的世界中，很常聽到雜湊，但你真的認識他嗎？

> 我們的認知雜湊是什麼？ 

- - Sha 系列 ： Sha0 、 Sha1 、Sha256 ... 等
- MD 系列 ： MD2 、 MD4 、MD5 ... 等

### 那雜湊到底在做什麼呢？

`主要是將不定長度訊息的輸入，演算成固定長度雜湊值的輸出，且所計算出來的雜湊值必須符合兩個主要條件`
- 雜湊值是無法還原成原來的訊息
- 雜湊會隨著明文改變而改變

> 那假如說真的算出兩個一樣的結果呢？
那這種情況我們稱之為碰撞（Collision），而這機率會是超級小。

![https://ithelp.ithome.com.tw/upload/images/20190924/20118325JRM1vWuLov.png](https://ithelp.ithome.com.tw/upload/images/20190924/20118325JRM1vWuLov.png)

若想嘗試雜湊可以來玩，[SHA256 online](https://emn178.github.io/online-tools/sha256.html)

### 那雜湊我們用在哪裡呢？

> 驗證密碼
大多數的程式像是 PHP 框架Laravel 的內建會員系統（他的存儲密碼方式就是使用雜湊），
因為雜湊只能出不能返回，很適合用作儲存密碼，使用者只有輸入正確的密碼才能解開。

> 區塊鏈系統驗證是否遭竄改
區塊鏈的系統中，一個區塊和一個區塊即是用雜湊來做串連，當內部有筆交易有問題則區塊的雜湊值即會改變，我們也能知道系統是否遭到竄改。

[Blockchain Demo](https://anders.com/blockchain/blockchain)

## 小記
經過這篇想必大家也了解，加密和雜湊的不同了！
簡單複習一下：
- 以非對稱加密為例，金鑰的作用可以進行簽章和加密訊息。
- 雜湊就像是一個果汁機，你丟什麼水果進去這個果汁機，他就會給你什麼果汁。

希望大家不要再說錯囉 XD

若文章有任何的問題或要討論的部分，歡迎在底下留言。
歡迎透過 Email: `kiss851990@gamil.com` 聯絡我。

## 資料來源
- [加密](https://blog.trendmicro.com.tw/?p=17075)
- [雜湊](https://zh.wikipedia.org/wiki/%E6%95%A3%E5%88%97)
- [Blockchain Demo](https://anders.com/blockchain/blockchain)
- [SHA256 online](https://emn178.github.io/online-tools/sha256.html)