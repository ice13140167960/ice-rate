# ice-star

## vue评分组件

## 使用方式

### 1.安装
```bash
npm i ice-star
```

### 2.main.js中全局注册组件

```js
import IceStar from 'ice-star';
Vue.use(IceStar);
```

### 3.使用组件
```vue
<ice-star
      :max="5"
      :count="count"
      @change="change"
      default-color="gray"
      select-color="#FFD566"
    ></ice-star>
```

```js
change(data){
  console.log(data);//当前分数
}
```

### API
#### 1.max:总分数，默认：5
#### 2.count:当前分数,默认：0
#### 3.default-color:未选中颜色,默认值:gray
#### 4.select-color:选中颜色,默认值:#FFD566

### Events

#### 1.change:分数改变事件，回传分数
