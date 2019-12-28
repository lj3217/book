# 小程序在 wepy框架 请求

## 数据请求

```javascript
// 页面加载
  onLoad() {
    // 调用获取轮播数据的方法
    this.getSwiperList()
  }

  // 获取轮播图的函数
  async getSwiperList () {
    // 发起请求获取轮播图数据   { data: res } 拿到数据以后，从数据对象中，把 data 解构出来，并命名为 res
    const { data: res } = await wepy.request({
      method: 'GET',
      url: 'https://uinav.com/api/public/v1/home/swiperdata'
    })

    // 判断是否请求成功
    if (res.meta.status !== 200) {
      // 请求失败：弹框提示用户，请求失败
      return wepy.showToast({
        title: '数据获取失败',
        // 不显示图标
        icon: 'none',
        // 多少秒后隐藏
        duration: 1500
      })
    }
    // 请求成功
    this.swiperList = res.message
    // 异步获取之后，需要调取 $apply()
    this.$apply()
    console.log(this)
  }
```

