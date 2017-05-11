# NPM 套件管理工具

* 類似 maven

### 初始化專案

**語法**

```
npm init [-f|--force|-y|--yes]
```

* 如果你加了 `-y` 或 `-f` 參數，代表你將認同使用預設的設定值來產生 `package.json` 檔。
* [init | nam Documentation](https://docs.npmjs.com/cli/init)

**範例**

```
npm init
npm init -y
npm init -f
```

**package.json**

* [package.json | nam Documentation](https://docs.npmjs.com/files/package.json)

```
{
  "name": "demo",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "license": "ISC"
}
```

**練習題**

使用 `npm init` 指令新增一個專案

### 安裝套件

* [install | npm Documentation](https://docs.npmjs.com/cli/install)
* 別名 i

**參數**

* -g：表示全域安裝
* --save：production
* --save-dev：development (預設)
* 什麼都沒加的情況

<!-- 示範有 -g -S 的情況，及沒有加 --save 的情況。 -->

**安裝專案下所有的套件**

```
cd your-project-folder
npm install
```

**安裝到專案，並將依賴寫入 package.json 的 devDependencies**

```
npm install --save-dev selenium-webdriver
```

### 執行 script

**package.json**

```
{
  "scripts":{
    "test":"node test.js"
  }
}
```

**test.js**

```
console.log('Hello World');
```