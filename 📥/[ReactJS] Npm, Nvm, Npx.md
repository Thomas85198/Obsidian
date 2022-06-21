## 何謂 npm
* Node Package Manager
* 會依據專案內的 package.json 去判定需要的依賴以及依賴的版本
---
## 何謂 nvm
* Node Version Manager
* 可以安裝多個不同的版本 Node 和 npm
### Mac OS 安裝
1. 於 Terminal 輸入下列指令
```shell=
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```
2. 於 bash/zsh 輸入環境變數，`vim ~/.zshrc`
```shell=
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh"] && \. "NVM_DIR/nvm.sh" # This loads nvm
[ -s "$NVM_DIR/bash_completion"] && \. "$NVM_DIR/bash_completion" #This loads nvm bash_completion
```
---
## nvm 指令介紹
```shell=
nvm ls-remote
```
* LTS (Long-term support) 穩定版
![[截圖 2022-06-21 12.19.23.png]]
```shell=
nvm install v12.18.3
```
### 決定好要安裝什麼版本
```shell=
nvm ls
```
![[截圖 2022-06-21 12.22.52.png]]
* default：每次專案套件的時候，都會預設執行的版本
* 若要切換指令 `nvm alias default v12.18.3`
* 若沒有要改變預設版本，只想改變當前 `nvm use v8.17.0`
> 若切換 Terminal nvm use 即失效
### 查看當前運行版本
```shell=
nvm current
```
> 雖然所有 Node 版本都在 NVM 中管理，但是各自下載的套件都是分開的
### Flag 旗標
* 在安裝 Node 版本時，指定套件一併安裝
* 我可以指定不同的版本都安裝某個套件
```shell=
nvm install v10.22.0 --reinstall-packages-form=v12.18.3
```
---
## 透過 npm 下載及管理套件
* 安裝、解除安裝與更新三個動作
```shell=
npm install -g create-reate-app
```
* -g 的意思是 global 不論在哪一個路徑下，只要打開 Terminal 就能直接使用
* 也可以只寫 `npm i`
* 如果安裝多個 `npm install <package> <package>`
* 區域安裝 `npm init`
### 初始化專案
```shell=
npm init
```
* 直接按 `Enter` 到底即可，只是輸入套件的基本資訊，若 Enter 到底即是輸入預設值
* 預設就會有一個 package.json
```shell=
npm install
```
* 產生  package-lock.json 與 node_modules
* dependencies：專案從開發到最後變成產品所使用的套件
* devDependencies：開發中使用的套件
### 安裝套件到 DevDependencies
```shell=
npm install <package> --save-dev
```
> --save 這個指令是將安裝的套件寫進 package.json，但現在不寫預設已經會寫入，若希望不寫入需要加上 --no-save 這個 flag
### 版本規則
* 若版本開頭加上^ e.g. ^16.14.1，代表會向上更新，有新的我會預設下載新的
	* 原本版本若 v1.2.3：v1.2.3-v2.0.0
	* 原本版本若 v0.1.2：v0.1.2-v0.2.0
	* 原本版本若 v0.0.1：v0.0.1
---
## Node_Modules
* 若 npm 全域安裝就是電腦任一個位置都能使用
* 區域環境就只能依賴專案的 scripts 去使用
![[Pasted image 20220621143808.png]]
執行就是輸入 `npm run test`就會執行後半段的指令
* 全域 node_module 預設路徑 /Users/luchienlin/.nvm/versions/node/v16.15.1
---
## 若要刪除套件
### 區域
```shell=
npm uninstall react
```
全域
```shell=
npm uninstall -g create-react-app
```
---
## 何謂 npx
* 不想要把套件下載到全域環境，只想做一次性使用
```shell=
npx <package>
```
