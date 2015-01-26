# Android开源框架分类
Android开源框架库分类，挑选出最常用，最实用的开源项目，本篇主要介绍的是优秀开源框架库和项目，UI个性化控件会独立介绍。
##Index
* [Networking](#networking)
	* [Android Lite Http](#android-lite-http)
	* [Asynchronous Http Client for Android](#asynchronous-http-client-for-android)
	* [Async Http Client](#async-http-client)
	* [HttpCache](#httpcache)
	* [Http Request](#http-request)
	* [Ion](#ion)
	* [OkHttp](#okhttp)
	* [Retrofit](#retrofit)
	* [Volley](#volley)
	* [Volley OkHttp Android](#volley_okHttp_android)

### Networking
#### [Android Lite Http](http://litesuits.com/) 
**Repository**: [https://github.com/litesuits/android-lite-http](https://github.com/litesuits/android-lite-http)  
**Description**: 一款‘智能’的HTTP框架类库。国人开发的一套框架。  
**Features**:  
* 单线程，所有方法都基于一个线程，绝不会跨线程，多线程的事情交给它自带的AsyncExecutor 或者更专业的框架库来解决。
* 灵活的架构，你可以轻松的替换Json自动化库、参数构建方式甚至默认的apache http client连接方式。
* 轻量级，微小的的开销，core jar包仅约86kb。
* 多种请求类型全面支持：get, post, head, put, delete, trace, options, patch.
* 多文件上传，不需要额外的类库支持。
* 内置的Dataparser支持文件和位图下载，你也可以自由的扩展DataParser来把原始的http inputstream转化为你想要的东西。
* 基于json的全自动对象转化： 框架帮你完成Java Object Model 和 Http Parameter之间的转化，完成Http Response与Java Object Model的转化。
* 自动重定向，基于一定的次数，不会造成死循环。
* 自动gizp压缩，帮你完成request编码和response解码以使http连接更加快速.
* 通过网络探测完成智能重试 ，对复杂的、信号不良的的移动网络做特殊的优化。
* 禁用一种或多种网络, 比如2G，3G。
* 简明且统一的异常处理体系：清晰、准确的抛出客户端、网络、服务器三种异常。
* 内置的AsyncExecutor可以让你轻松实现异步和并发的http请求，如果你喜欢，随意使用你自己的AsyncTask或Thread来完成异步，推荐使用更强大、高效的专业并发库。 

#### [Asynchronous Http Client for Android](http://loopj.com/android-async-http/) 
**Repository**: [https://github.com/loopj/android-async-http](https://github.com/loopj/android-async-http)  
**Description**: Android异步Http请求  
**Used By**:
  * [Instagram](https://play.google.com/store/apps/details?id=com.instagram.android)
  * [Pinterest](https://play.google.com/store/apps/details?id=com.pinterest)
  * [Frontline Commando](https://play.google.com/store/apps/details?id=com.glu.modwarsniper)
  * [Thousands more apps…](http://www.appbrain.com/stats/libraries/details/loopj_asynchttpclient/android-asynchronous-http-client)

**Features**:
* 在匿名回调中处理请求结果
* 在UI线程外进行http请求
* 请求使用ThreadPool来处理并非资源的使用
* 文件断点上传
* 智能重试
* 默认gzip压缩
* 内置Json解析
* 可将Cookies持久化到SharedPreferences
* [More](https://github.com/loopj/android-async-http#features)

#### [Async Http Client](https://asynchttpclient.github.io/async-http-client/)  
**Repository**: [https://github.com/AsyncHttpClient/async-http-client](https://github.com/AsyncHttpClient/async-http-client)  
**Description**: Java异步Http和WebSocket请求。使用NIO实现异步操作，默认的异步实现是基于[Netty]()之上。 
#### [HttpCache](http://www.trinea.cn/android/android-http-cache) 
**Repository**: [https://github.com/Trinea/AndroidCommon](https://github.com/Trinea/AndroidCommon)  
**Description**: [Trinea](https://github.com/Trinea)大神写的Http缓存工具。 
**Features**:
* 根据cache-control、expires缓存http请求
* 支持同步、异步Http请求
* 在匿名回调中处理请求结果
* 在UI线程外进行http请求
* 默认gzip压缩

#### [Http Request](https://github.com/kevinsawicki/http-request) 
**Repository**: [https://github.com/kevinsawicki/http-request](https://github.com/kevinsawicki/http-request)  
**Description**: Java HTTP请求库。 

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
  
#### [Retrofit](http://square.github.io/retrofit/) 
**Repository**: [https://github.com/square/retrofit](https://github.com/square/retrofit)  
**Description**: Square开源的Android和Java的REST风格请求库. 

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

#### [Volley OkHttp Android](https://github.com/lxdvs/Volley-OkHttp-Android/)  
**Repository**: [https://github.com/lxdvs/Volley-OkHttp-Android](https://github.com/lxdvs/Volley-OkHttp-Android)  
**Description**: 整合OkHttp和Volley。 

<a href="#networking" title="返回目录" style="width:100%"><img src="https://raw.githubusercontent.com/yeungeek/awesome-android-libraries/master/art/ic_arrow.png" align="right"/></a>
## Reference
*  [android-arsenal](https://android-arsenal.com/)
*  [Trinea android-open-project](https://github.com/Trinea/android-open-project)
*  [wasabeef awesome-android-libraries](https://github.com/wasabeef/awesome-android-libraries)

<a href="#index" title="返回目录" style="width:100%"><img src="https://raw.githubusercontent.com/yeungeek/awesome-android-libraries/master/art/ic_arrow.png" align="right"/></a>
