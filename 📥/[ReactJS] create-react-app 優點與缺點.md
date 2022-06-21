## React 開發環境
### create-react-app 的優點與缺點
   | 優點                                                | 缺點                                 |
   | --------------------------------------------------- | ------------------------------------ |
   | 不用懂太多，能專注在開發，預設就給你一個 React 專案 | 預設會載入的無法調整，不管你有無用到；反之若新技術要使用也無法去調整像是 Webpack 或 Babel 等設定 |
- Facebook 開發的開源工具
### npm run eject
- 當想要修改 create-react-app 內部設定時
```shell=
npm run eject
```
執行指令後，便會將 webpack、Babel 等預設的配置文件，都複製到根目錄進行修改
> Note: this is a one-way operation. Once you eject, you can't go back