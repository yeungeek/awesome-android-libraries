# Android开源框架分类
Android开源框架库分类，挑选出最常用，最实用的开源项目，本篇主要介绍的是优秀开源框架库和项目，UI个性化控件会独立介绍。
##Index
* [Networking](#networking)
	* [Asynchronous Http Client for Android](#asynchronous-http-client-for-android)
	* [Async Http Client](#async-http-client)
	* [Ion](#ion)
	* [OkHttp](#okhttp)

### Networking
#### [Asynchronous Http Client for Android](http://loopj.com/android-async-http/) 
**Repository**: [https://github.com/loopj/android-async-http](https://github.com/loopj/android-async-http)  
**Description**: Android异步Http请求  
**Used By**:
  * [Instagram](https://play.google.com/store/apps/details?id=com.instagram.android)
  * [Pinterest](https://play.google.com/store/apps/details?id=com.pinterest)
  * [Frontline Commando](https://play.google.com/store/apps/details?id=com.glu.modwarsniper)
  * [Thousands more apps…](http://www.appbrain.com/stats/libraries/details/loopj_asynchttpclient/android-asynchronous-http-client)

**Features**:
  1. 在匿名回调中处理请求结果
  2. 在UI线程外进行http请求
  3. 请求使用ThreadPool来处理并非资源的使用
  4. 文件断点上传
  5. 智能重试
  6. 默认gzip压缩
  7. 内置Json解析
  8. 可将Cookies持久化到SharedPreferences
  9. [More](https://github.com/loopj/android-async-http#features)

#### [Async Http Client](https://asynchttpclient.github.io/async-http-client/)  
**Repository**: [https://github.com/AsyncHttpClient/async-http-client](https://github.com/AsyncHttpClient/async-http-client)  
**Description**: Java异步Http和WebSocket请求。使用NIO实现异步操作，默认的异步实现是基于[Netty]()之上。 
#### [Ion](https://github.com/koush/ion)
**Repository**: https://github.com/koush/ion  
**Description**: Android异步网络和图片加载.   
**Used By**: [https://github.com/koush/ion#projects-using-ion](https://github.com/koush/ion#projects-using-ion)  
**Features**: [https://github.com/koush/ion#features](https://github.com/koush/ion#features)  
#### [OkHttp](http://square.github.io/okhttp/)  
**Repository**: [https://github.com/square/okhttp](https://github.com/square/okhttp)  
**Description**: Square开源的http库，支持http和spdy协议.  
**Features**:
  1. 支持HTTP2和[SPDY](http://zh.wikipedia.org/wiki/SPDY)
  2. 如果SPDY不可用，利用连接池减少请求延迟
  3. 使用GZIP压缩
  4. Response缓存减少不必要的请求  

#### [Volley](https://android.googlesource.com/platform/frameworks/volley)
**Repository**: [google volley](https://android.googlesource.com/platform/frameworks/volley) | [https://github.com/mcxiaoke/android-volley](https://github.com/mcxiaoke/android-volley)  
**Description**: Google提供的网络通信库，使得网络请求更简单、更快速  
**Features**:  
  1. JSON，图像等的异步下载
  2. 网络请求的排序
  3. 网络请求的优先级处理
  4. 缓存 
  5. 多级别取消请求
  6. 和Activity和生命周期的联动（Activity结束时同时取消所有网络请求）
  7. [More](http://commondatastorage.googleapis.com/io-2013/presentations/110%20-%20Volley-%20Easy,%20Fast%20Networking%20for%20Android.pdf) 

<a href="https://github.com/yeungeek/awesome-android-libraries#networking" title="返回目录" style="width:100%"><img src="https://raw.githubusercontent.com/yeungeek/awesome-android-libraries/master/art/ic_arrow.png" align="right"/></a>
## Reference
*  [android-arsenal](https://android-arsenal.com/)
*  [Trinea android-open-project](https://github.com/Trinea/android-open-project)
*  [wasabeef awesome-android-libraries](https://github.com/wasabeef/awesome-android-libraries)
