# Description
```
This is a Vue component for checkbox
```
# Install

``` 
npm install wl-checkbox
```
# Use

```
# In main.js
import WlCheckbox from 'wl-checkbox'
Vue.use(WlCheckbox)

# In *.vue
<wl-checkbox></wl-checkbox>  
```
# Attributes

参数 | 说明 | 类型 | 可选值 |  默认值  
---- | ---- | ---- | ---- | ---- 
checked | 是否选中 | Boolean | true/false | false
disabled | 是否禁用 | Boolean | true/false | false
className | 自定义 class | String | |
label | 自定义描述 | String | |


# Events

事件| 说明 | 参数 
----| ---- | ----  
change | 监听checked状态    |  `checked` - 返回被选中状态   
 

 
 
