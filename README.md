# Laravel 9 程式品質分析器

引入 nunomaduro 的 phpinsights 套件來擴增分析程式品質，可以很簡單的方式從終端機直接進行分析。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 對程式碼進行一系列評分，包括複雜程度，應用程式結構等一些細項。
```sh
$ php artisan insights
```

----

## 畫面截圖
![](https://i.imgur.com/Za0OJXl.png)
> 進行即時質量檢查，使程式碼可靠、簡潔且鬆散耦合
