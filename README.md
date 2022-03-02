
# URL Scheme 

### IOS
URL Scheme就是一个可以让 APP 相互之间可以跳转的协议。每个 APP 的URL Scheme都是不一样的，如果存在一样的URL Scheme，那么系统就会响应先安装那个 APP 的URL Scheme，因为后安装的 APP 的URL Scheme被覆盖掉了，是不能被调用的。

### Android 
Android中的 Scheme 是一种页面内跳转协议，是一种非常好的实现机制，通过定义自己的 Scheme 协议，可以非常方便跳转app中的各个页面；通过scheme协议，服务器可以定制化告诉App跳转那个页面，可以通过通知栏消息定制化跳转页面，可以通过H5页面跳转页面等。
URL Scheme 就如同网页的url链接一样，可以打开App或跳转到相应的页面。但是大部分APP没有公开自己的URL Scheme。

## 常用iOS APP的 URL Scheme

收集了一些常用iOS APP的 URL Scheme 及示例，持续更新，欢迎大家一起来补充。

系统
--

    设置 (App调用可添加“App-”前缀）
    电池电量 Prefs:root=BATTERY_USAGE
    存储空间 Prefs:root=General&path=STORAGE_ICLOUD_USAGE/DEVICE_STORAGE
    蜂窝数据 Prefs:root=MOBILE_DATA_SETTINGS_ID
    Wi-Fi 设置 Prefs:root=WIFI![]()
    蓝牙设置 Prefs:root=Bluetooth
    定位设置 Prefs:root=Privacy&path=LOCATION
    辅助功能 Prefs:root=General&path=ACCESSIBILITY
    关于手机 Prefs:root=General&path=About
    键盘设置 Prefs:root=General&path=Keyboard
    显示设置 Prefs:root=DISPLAY
    声音设置 Prefs:root=Sounds
    App Store 设置 Prefs:root=STORE
    墙纸设置 Prefs:root=Wallpaper
    
    捷径 workflow://run-workflow?name=[name]&input=[input]   !2018.10.31
    世界时钟 Clock-worldclock://
    闹钟 Clock-alarm://
    秒表 Clock-stopwatch://
    倒计时 Clock-timer://
    打开相册 Photos://
    查找iPhone fmip1://
    打电话 tel://110
    备忘录 mobilenotes://
    日历 calshow://
    AppStore 
      查看某app https://itunes.apple.com/cn/app/id741597322?mt=8
      搜索 https://itunes.apple.com/WebObjects/MZStore.woa/wa/search?mt=8&submit=edit&term=微信#software
    

工具
--

    Chrome googlechrome://
    手机百度 BaiduSSO://
    QQ浏览器 mqqbrowser://
    uc浏览器 ucbrowser://
    搜狗输入法 com.sogou.sogouinput://
    圈子账本 qzzb://
    我的密码 findmykey://
    我查查 wcc://
    有道词典 yddict://
    名片全能王 camcard://
    Evernote evernote://
    迅雷 thunder://
    QQ同步助手 qqpim://
    天气通 sinaweather://
    墨迹天气 rm434209233MojiWeather://
    同花顺 amihexin://
    腾讯企业邮箱 qqbizmailDistribute2://
    腾讯手机管家 mqqsecure://
    网易邮箱 neteasemail://
    百度云 baiduyun:// 
    

**社交**
------

    知乎 zhihu://    !2018.10.31更新
    （某篇文章）zhihu://articles/27758684
    （某个专栏）zhihu://columns/lishuai
    QQ mqq://
    微信 
        weixin://
      (扫一扫)weixin://scanqrcode 
    微博 
    微博国际版 weibointernational:       感谢 @MrClown 贡献
    （热搜）weibointernational://hotsearch
    百度贴吧 com.baidu.tieba://
    腾讯微博 TencentWeibo://
    陌陌 momochat://
    天涯社区 tianya://
    探探 tantanapp://

购物
--

    淘宝 taobao://
      (搜索)taobao://s.taobao.com/?q=裙子
    支付宝 alipay:// 
      (付款) alipayqr://platformapi/startapp?saId=20000056
      (扫一扫) alipayqr://platformapi/startapp?saId=10000007
      (打开收款) alipays://platformapi/startapp?appId=20000123
      (打开 AA 收款) alipays://platformapi/startapp?appId=20000263
      (打开付款) alipay://platformapi/startapp?appId=20000056
      (打开转账) alipayqr://platformapi/startapp?saId=20000116
      (打开二维码扫一扫) alipayqr://platformapi/startapp?saId=10000007
      (打开乘车码) alipayqr://platformapi/startapp?saId=200011235
      (打开记账) alipay://platformapi/startapp?appId=20000168
      (打开红包) alipays://platformapi/startapp?appId=88886666
      (打开滴滴) alipay://platformapi/startapp?appId=20000778
      (打开蚂蚁森林) alipay://platformapi/startapp?appId=60000002
      (打开手机充值) alipayqr://platformapi/startapp?saId=10000003
      (打开生活缴费) alipays://platformapi/startapp?appId=20000193
      (打开彩票) alipays://platformapi/startapp?appId=10000011
      (打开股票) alipays://platformapi/startapp?appId=20000134
      (打开快递查询) alipays://platformapi/startapp?appId=20000754
      (打开还信用卡) alipays://platformapi/startapp?appId=09999999

    京东 openapp.jdmobile://
    美团 imeituan://
    大众点评 dianping://
    1号店 yhd://
    唯品会 vipshop://
    拼多多 pinduoduo://


    

出行
--

    高德地图 
      (公交导航)iosamap://path?sourceApplication=日历&sid=BGVIS1&sname=$我的位置&did=BGVIS2&dname=目的地&dlat=纬度&dlon=经度&dev=0&m=0&t=0  
    // t为出行方式：0 驾车，1 公交，2 步行 
    // m为出行要求 当t为驾车时：0速度最快，1费用最少，2距离最短，3不走高速，4躲避拥堵，5不走高速且避免收费，6不走高速且躲避拥堵，7躲避收费和拥堵，8不走高速躲避收费和拥堵 
    当t为公交时：0最快捷，2最少换乘，3最少步行，5不乘地铁 ，7只坐地铁 ，8时间短  
    
    百度地图 baidumap://
      (导航)baidumap://map/direction?origin=我的位置&destination=公司&mode=driving 
    //mode 导航模式，固定为transit、driving、walking
    腾讯地图 qqmap://
      (导航）qqmap://map/routeplan?from=我的位置&type=drive&tocoord=36.547901,104.258354&to=dest&coord_type=1&policy=0
    北京交警 zcblbjjj://
    滴滴出行 diditaxi://
    摩拜单车扫码 mobike://scanqr
    订票助手 trainassist://
    艺龙旅行 elongIPhone://
    携程无线 CtripWireless://
    淘宝旅行 taobaotravel://
    

娱乐
--

    优酷 youku://
    爱奇艺视频 qiyi-iphone://
    PPTV pptv://
    今日头条 snssdk141://
    哔哩哔哩动画 bilibili://
    优酷 youku://
    搜狐视频 sohuvideo://
    腾讯视频 tenvideo://
    掌阅iReader iReader://
    网易新闻 newsapp://
    腾讯新闻 qqnews://
    网易云音乐 orpheus://   !2018.10.31更新
      (识别音乐)orpheus://recognize
    （本地音乐）orpheus://download
    （私人FM）orpheus://radio
    （我的喜欢）orpheus://playlist/32778108  !歌单编号可以通过分享歌单的链接获得2018.10.31更新
    QQ音乐 qqmusic://
    豆瓣FM doubanradio://
    百度音乐 baidumusic://
    百度视频 baiduvideoiphone://
    抖音 awemesso://
    西瓜视频 snssdk32://
    一直播 xktv://
    花椒直播 huajiao://
    

其他
--

    招商银行 cmbmobilebank://
    建设银行 wx2654d9155d70a468://
    工商银行 com.icbc.iphoneclient://
    浦发银行 wx1cb534bb13ba3dbd://

    沪江词典 hjdict://
    菜鸟锅锅 cainiao://
    百度网盘 baiduyun://
    360搜索 msearchapp://
    搜狗搜索 sogousearch://
    下厨房 xcfapp://
    钉钉 dingtalk://
    拿铁阅读 LatteRead://
    网易公开课 neteaseVopen://
    一席 wx5bc45646a79e74ab://

    诗词之美   xcz-lean://
    多点会员码   memberNumberDesktop://
    多点扫码   scanDesktop://
    京东 双签（须先用京东签到）   jdmobile://share?jumpType=7&jumpUrl=1373
    京东签到   openApp.jdMobile://virtual?params={"category":"jump","modulename":"JDReactCollectJDBeans","des":"jdreactcommon","param":{"page":"collectJDBeansHomePage";}}
    





    
    
### 资料：
- [URL Schemes 使用详解](https://sspai.com/post/31500)
- [URL Scheme shared](https://st3376519.huoban.com/share/1985010/VGi2N5Vf0C1MVnHCVWiBc8L9g15c9VGJbMGcFrb6/172707/list)
- [https://gist.github.com/JamesHopbourn/046bc341e7debfd0c86e3b388d983c53](https://gist.github.com/JamesHopbourn/046bc341e7debfd0c86e3b388d983c53)
- [https://github.com/shyrz/url-schemes-store](https://github.com/shyrz/url-schemes-store)

