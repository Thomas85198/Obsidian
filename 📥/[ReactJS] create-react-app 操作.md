## create-react-app
執行以下指令，安裝一個 React.js 的專案
```shell=
npx create-react-app <name>
```
![[Pasted image 20220621164231.png]]
專案的預設目錄
### 解析專案目錄
- public：存放了負責輸出的 HTML 檔案，放一些靜態的資源，webpack 打包不會去處理
- src：程式碼的主要內容，甚至還有單元測試的檔案（副檔名為 `.test.js`）
### 執行專案
```shell=
npm run start
```
### 打包專案
```shell=
npm run build
```
- 打包完的程式會放在 build 資料夾內
### 運行測試
```shell=
npm run test
```
- `a`：全部測試
- `f`：只測試失敗的
- `q`：退出不測了
- `p`和`t`：用正規表達式來找要測試的檔案
- Enter：開啟監聽模式，檔案異動，馬上測試
