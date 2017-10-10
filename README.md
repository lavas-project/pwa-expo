# pwa-expo

PWA 相关特性支持度的说明文件，关注国内主流浏览器。

数据将更新在 ([Lavas 官网](https://lavas.baidu.com/ready))



## 数据格式

`feature.json` 各特性支持度的备注说明

``` javascript
{
    "features": [
        {
            "name": "Promise", // 特性名称
            "infos": [
                "UC 手机浏览器: Window 域中暂未实现" // 备注说明，多条使用英文逗号『,』分隔
            ]
        }
        // ...
    ]
}
```

`manifest.json` 不同 rom 添加到桌面功能支持情况

``` javascript
{
    "manifest": [
        {
            "brand": "华为", // rom 对应的手机品牌
            "device": "P8", // 设备型号
            "rom": "EMUI", // rom 类型
            "detail": [
                "360：可见添加至桌面按钮，但属快捷方式", // 备注说明，多条使用英文逗号『,』分隔
                "QQ/搜狗/猎豹/2345/Opera：目前浏览器未暴露添加桌面入口"
            ],
            "browser": [
                {
                    "name": "Chrome", // 浏览器名称，注：均使用最新版本测试
                    "score": 1 // 1 支持，0 不支持
                }
                // ... 更多浏览器
            ]
        }
        // ... 更多品牌
    ]
}
```

