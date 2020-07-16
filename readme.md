## vite体验vue3

这是尤大开发的新工具，目的是以后取代 webpack，原理就是利用浏览器现在已经支持 es6 的 import 了，碰见 import 会发送一个 http 请求去加载文件，vite 拦截这些请求，做一些预编译，就省去了 webpack 冗长的打包时间，提升开发体验
推荐体验
先体验一下

```sh
npm install -g create-vite-app
create-vite-app vue3-vite-01
cd vue3-vite-01
npm install
npm run dev
```

