# ice-rate

## vue评分组件

## 使用方式

### 1.安装
```bash
npm i ice-rate
```

### 2.main.js中全局注册组件

```js
import IceRate from 'ice-rate';
Vue.use(IceRate);
```

### 3.使用组件
```vue
<ice-rate
      :max="5"
      v-model="value"
      default-color="gray"
      select-color="#FFD566"
    ></ice-rate>
```

### API
#### 1.max:总分数，默认：5
#### 2.v-model:当前分数,默认：0
#### 3.default-color:未选中颜色,默认值:gray
#### 4.select-color:选中颜色,默认值:#FFD566
#### 5.readonly:是否只读，默认值：false
