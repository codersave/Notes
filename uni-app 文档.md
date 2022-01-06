# uni-app基础
###  规范
##### 页面文件遵循Vue单文件组件规范:
```vue
<template>
    <view class="main">
        {{msg}}	
    </view>
</template>

<script>
	export default {
        data() {
            return {
				msg: 'Hello'
            }
        }
    }
</script>

<style>
    .main {
        background-color: #f5f5f5;
    }
</style>

```

##### 组件标签靠近小程序规范：

```html
<!-- 传统标签 -->
<body>
	<div>Hello</div>
	<span>Tom</span>
</body>

<!-- 组件标签 -->
<template>
	<view>Hello</view>
    <text>Tom</text>
</template>
```

##### 接口能力(JS API)靠近微信小程序规范：

```javascript
// 获取位置信息
uni.getLocation({
    type: 'wgs84',
    success: function(res) {
        console.log('当前经度：'+res.longitude);
        console.log('当前纬度：'+res.latitude);
    }
})
```

##### 数据绑定与事件处理使用Vue.js规范：

```vue
<template>
	<view @click="changeMsg">
    	{{msg}}
    </view>
</template>

<script>
	export default {
        data() {
            return {
                msg: 'Hello'
            }
        },
        methods: {
            changeMsg() {
                this.msg = 'Nice'
            }
        }
    }
</script>

<style></style>
```

### 特色

##### 条件编译

![uniapp_if](./assets/uniapp_if.png)



