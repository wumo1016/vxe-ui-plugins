# @vxe-ui/plugin-render-naive

[Vxe UI](https://vxeui.com/) plug-in for compatibility with the [naive-ui](https://www.npmjs.com/package/naive-ui) component.

## Compatibility

It corresponds to [vxe-table v4](https://www.npmjs.com/package/vxe-table) or [vxe-pc-ui v4](https://www.npmjs.com/package/vxe-pc-ui)  

## Installing

```shell
npm install @vxe-ui/plugin-render-naive
```

```javascript
// ...
// Use vxe-pc-ui
import { VxeUI } from 'vxe-pc-ui'
// Use vxe-table
// import { VxeUI } from 'vxe-table'
import VxeUIPluginRenderNaive from '@vxe-ui/plugin-render-naive'
import '@vxe-ui/plugin-render-naive/dist/style.css'
// ...

VxeUI.use(VxeUIPluginRenderNaive)
```

## API

## Table Cell demo

```html
<vxe-table
  height="600"
  :data="tableData"
  :edit-config="{trigger: 'click', mode: 'cell'}">
  <vxe-column field="name" title="Name" :edit-render="{}">
    <template #edit="{ row }">
      <n-input v-model:value="row.name"></n-input>
    </template>
    <template #default="{ row }">
      <span>{{ row.name }}</span>
    </template>
  </vxe-column>
  <vxe-column field="age" title="Age" :edit-render="{}">
    <template #edit="{ row }">
      <n-input v-model:value="row.age"></n-input>
    </template>
    <template #default="{ row }">
      <span>{{ row.age }}</span>
    </template>
  </vxe-column>
  <vxe-column field="date" title="Date" width="200" :edit-render="{}">
    <template #edit="{ row }">
      <n-date-picker type="date" v-model:value="row.date"></n-date-picker>
    </template>
    <template #default="{ row }">
      <span>{{ row.date }}</span>
    </template>
  </vxe-column>
</vxe-table>
```

## Contributors

Thank you to everyone who contributed to this project.

[![vxe-ui-plugins](https://contrib.rocks/image?repo=x-extends/vxe-ui-plugins)](https://github.com/x-extends/vxe-ui-plugins/graphs/contributors)

## License

[MIT](LICENSE) © 2019-present, Xu Liangzhan
