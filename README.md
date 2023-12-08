# 快速开始

本节将介绍如何在项目中使用 YS-UI。

## 文档地址 [ys-ul-docs](https://zhaoxianzhao.github.io/ys-ui-docs/)

## 用法

### 插件依赖

使用 unocss 样式库，有对应的vscode插件，请自行安装 [安装文档](https://blog.csdn.net/halo1416/article/details/131162456)

[css类名查找文档](https://unocss.dev/interactive/)

### 完整引入

如果你对打包后的文件大小不是很在乎，那么使用完整导入会更方便。

```ts
// main.ts
import { createApp } from 'vue'
import YsUi from 'ys-ui'
import 'ys-ui/dist/index.css'
import App from './App.vue'

const app = createApp(App)

app.use(YsUi)
app.mount('#app')
```

### 按需引入

```ts
// main.ts
import { YsPagination } from 'ys-inside-ui'
// 不管全局还是按需，都需要再主入口引入样式文件
import 'ys-inside-ui/lib/style.css'
```

> app.vue
```html
<!-- .vue文件引入 -->
<script setup lang="ts">
  import { TDetail, TForm } from 'ys-inside-ui'
</script>
```

### Volar 组件类型提示
如果您使用 Volar，请在 `tsconfig.json` 中通过 `compilerOptions.types` 指定全局组件类型。

:::warning 注意，有警告！ ⚡️

目前呢 还有点问题；支持度只支持了按需引入，全局的正在处理
:::

```json
// tsconfig.json
{
  "compilerOptions": {
    // ...
    "types": ["ys-inside-ui/components.d.ts"]
  }
}
```
