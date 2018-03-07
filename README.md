#### Https页面不再支持http协议资源（资源加载失败等）
- 确保引入资源符合协议正确，https降级支持http逻辑已经移除，`http://g.tbcdn.cn/` 需要统一更换为 `https://g.alicdn.com` 例如：`https://g.alicdn.com/sj/qn/jssdk-ex-debug.js`
- 建议使用自适应protocol，如`//g.alicdn.com/sj/qn/jssdk-ex-debug.js`，此时资源协议将与页面保持一致，阿里的CDN支持双协议

#### qntag缓存失效，拉取资源size为0
表现现象为：
![IMAGE](https://img.alicdn.com/tfs/TB1h0EfcXOWBuNjy0FiXXXFxVXa-1116-493.png)

#### 布局异常（不推荐及可能出现异常的css写法）
- 混用弹性+百分比布局（推荐使用标准flex实现，移除百分比逻辑）， 依然使用渐进增强（flex已全量支持，请使用flex标准，去掉兼容性前缀）
![IMAGE](https://img.alicdn.com/tfs/TB1kMwfceSSBuNjy0FlXXbBpVXa-1396-688.png)




