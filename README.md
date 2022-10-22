<div align="center">
  <a href="https://dom-to-code.netlify.app/">
    <img src="https://raw.githubusercontent.com/better-tcy/dom-to-code/master/packages/doc/.vuepress/public/images/logo.png" width="50%">
  </a>
  <div align="center">

# Dom To Code

  <p>屎山救星，点击 dom 直接跳到编辑器对应代码。支持 vite/webpack、vue2/vue3/react</p>

  </div>
  
  <p>
    <a href="https://www.npmjs.com/package/dom-to-code"><img src="https://img.shields.io/npm/v/dom-to-code.svg" alt="npm package"></a>
  <a href="#badge"><img src="https://img.shields.io/github/languages/top/better-tcy/dom-to-code" alt="language"></a>
  <a href="https://img.badgesize.io/https:/unpkg.com/dom-to-code/dist/js/index.es.js?label=gzip%20size&compression=gzip"><img src="https://img.badgesize.io/https:/unpkg.com/dom-to-code/dist/js/index.es.js?label=gzip%20size&compression=gzip" alt="gzip"></a>
  <a href="#badge"><img src="https://img.shields.io/librariesio/github/better-tcy/dom-to-code" alt="librariesio"></a>
  <a href="https://github.com/better-tcy/dom-to-code/blob/master/LICENSE"><img src="https://img.shields.io/github/license/better-tcy/dom-to-code" alt="LICENSE"></a>
    <img src="https://img.shields.io/github/stars/better-tcy/dom-to-code?style=social" alt="stars">
  </p>
</div>

## ✨ 介绍

受够了翔一般的代码，每次想改一下接手的项目都得各种搜索代码来改，于是就有了这个屎山救星。

引入插件到项目后，ctrl + 按下鼠标滚轮，就会在编辑器打开鼠标下的界面元素源码。

别人搜索你直接跳，别人加班你摸鱼。

## 📦 安装

```bash
npm i -D dom-to-code
```

## 🔨 使用

<details>
<summary>Vite</summary><br>

```ts
// vite.config.ts
import { defineConfig } from 'vite'
import vue3 from '@vitejs/plugin-vue'
import { domToCodePlugin } from 'dom-to-code/vite'

export default defineConfig({
  plugins: [
    vue3(),
    domToCodePlugin({
      /* options */
    })
  ]
})
```

Example: [`playgrounds/vite-vue3`](./playgrounds/vite-vue3/)

<br></details>

<details>
<summary>Vue CLI</summary><br>

```ts
// vue.config.js
const { domToCodePlugin, domToCodeDevServerV4, domToCodeDevServerV5 } = require('dom-to-code/webpack')

module.exports = {
  devServer: {
    // 如果你的 package.json 里的 @vue/cli-service 版本 <= 4.x.x，则使用 domToCodeDevServerV4
    // ...domToCodeDevServerV4,

    // 如果你的 package.json 里的 @vue/cli-service 版本 >= 5.x.x，则使用 domToCodeDevServerV5
    ...domToCodeDevServerV5
  },
  configureWebpack: {
    plugins: [
      domToCodePlugin({
        /* options */
      })
    ]
  }
}
```

Example: [`playgrounds/webpack-vue2`](./playgrounds/webpack-vue2/)

<br></details>

<details>
<summary>Webpack</summary><br>

```ts
// webpack.config.js
const { domToCodePlugin } = require('dom-to-code/webpack').default
module.exports = {
  /* ... */
  plugins: [
    domToCodePlugin({
      /* options */
    })
  ]
}
```

<br></details>

## 📚 文档

查看 [文档指南 📒](https://dom-to-code.netlify.app/)(即将上线...)

## 💡 注意

如果无法跳转编辑器，请确保你的编辑器已经添加到环境变量，比如 vscode，添加成功后在命令终端输入

```bash
code -v
```

可以看到 vscode 版本信息意味着成功。

## 🤖️ Contributing

Learn about contribution [here](https://github.com/better-tcy/dom-to-code/blob/master/CONTRIBUTING.md).

This project exists thanks to all the people who contribute:

<a href="https://github.com/better-tcy/dom-to-code/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=better-tcy/dom-to-code" />
</a>

## 🌸 Credits

- [unplugin](https://github.com/unjs/unplugin)

- [vite-plugin-react-inspector](https://github.com/sudongyuer/vite-plugin-react-inspector)

- [vite-plugin-vue-inspector](https://github.com/webfansplz/vite-plugin-vue-inspector)

## 📄 License

[MIT](https://github.com/better-tcy/dom-to-code/blob/master/LICENSE) License © 2022-PRESENT [tuocangyu](https://github.com/better-tcy)
