# Android开源框架分类
Android开源框架库分类，挑选出最常用，最实用的开源项目，本篇主要介绍的是优秀开源框架库和项目，UI个性化控件会独立介绍。
##Index
* [Dependency Injections](#dependency-injections)
    * [AndroidAnnotations](#androidannotations)
    * [Butter Knife](#butter-knife)
    * [Dagger](#dagger)
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
	* [Volley OkHttp Android](#volley_okhttp_android)
* [Image Loader](#image-loader)
    * [Cube SDK](#cube-sdk)
    * [Glide](#glide)
    * [ImageCache](#imagecache)
    * [Picasso](#picasso)
    * [Universal Image Loader for Android](#universal-image-loader-for-android)
* [O/R Mapping]
* [Event Buses]
* [JSON]
* [Backward Compatibility]
* [Background Processing]
* [Image Processing]
* [Camera]
* [Video]
* [Logging]
* [Android Plugin]
* [NoSQL]
* [Security]
* [Showcases]

### Dependency Injections
#### [AndroidAnnotations](http://androidannotations.org/)
**Repository**: [https://github.com/excilys/androidannotations](https://github.com/excilys/androidannotations)  
**Description**: android快速开发框架。  
**Features**:  
* 依赖注入：包括view，extras，系统服务，资源等等
* 简单的线程模型，通过annotation表示方法运行在ui线程还是后台线程
* 事件绑定：通过annotation表示view的响应事件，不用在写内部类
* REST客户端：定义客户端接口，自动生成REST请求的实现
* 没有你想象的复杂：AndroidAnnotations只是在在编译时生成相应子类
* 不影响应用性能：仅50kb，在编译时完成，不会对运行时有性能影响。  

> PS：与roboguice的比较：roboguice通过运行时读取annotations进行反射，所以可能影响应用性能，而AndroidAnnotations在编译时生成子类，所以对性能没有影响。  

#### [Butter Knife](http://jakewharton.github.io/butterknife/)
**Repository**: [https://github.com/JakeWharton/butterknife](https://github.com/JakeWharton/butterknife)  
**Description**: JakeWharton的开源作品，利用annotation帮你快速完成View的初始化，减少代码。  
**Features**:  
* 支持 Activity 中的 View 注入
* 支持 View 中的 View 注入
* 支持 View 事件回调函数注入

#### [Dagger](http://square.github.io/dagger/)
**Repository**: [https://github.com/square/dagger](https://github.com/square/dagger)  
**Description**: sqaure开源的依赖注入框架，是Guice的一个子集，更轻量，更适合在Android平台使用。  
**Features**:  
* 使用 JSR-330标准注解进行构造器注入
* 使用@Provides注解创建对象
* 针对依赖树的中心上下文
* 昂贵资源延迟注入
* 同一接口的多种实现
* 静态注入 (针对遗留环境)
* 绑定的编译时验证

> 依赖注入框架的对比：[dagger-and-butter-knife-vs-android-annotations](http://stackoverflow.com/questions/24351817/dagger-and-butter-knife-vs-android-annotations),[依赖注入浅析](http://blog.csdn.net/tryit1993/article/details/40210687)

<a href="#dependency-injections" title="返回目录" style="width:100%"><img src="https://raw.githubusercontent.com/yeungeek/awesome-android-libraries/master/art/ic_arrow.png" align="right"/></a>
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
* 支持HTTP2和[SPDY](http://zh.wikipedia.org/wiki/SPDY)
* 如果SPDY不可用，利用连接池减少请求延迟
* 使用GZIP压缩
* Response缓存减少不必要的请求  
  
#### [Retrofit](http://square.github.io/retrofit/) 
**Repository**: [https://github.com/square/retrofit](https://github.com/square/retrofit)  
**Description**: Square开源的Android和Java的REST风格请求库. 

#### [Volley](https://android.googlesource.com/platform/frameworks/volley)
**Repository**: [google volley](https://android.googlesource.com/platform/frameworks/volley) | [https://github.com/mcxiaoke/android-volley](https://github.com/mcxiaoke/android-volley)  
**Description**: Google提供的网络通信库，使得网络请求更简单、更快速  
**Features**:  
* JSON，图像等的异步下载
* 网络请求的排序
* 网络请求的优先级处理
* 缓存 
* 多级别取消请求
* 和Activity和生命周期的联动（Activity结束时同时取消所有网络请求）
* [More](http://commondatastorage.googleapis.com/io-2013/presentations/110%20-%20Volley-%20Easy,%20Fast%20Networking%20for%20Android.pdf) 

#### [Volley OkHttp Android](https://github.com/lxdvs/Volley-OkHttp-Android/)  
**Repository**: [https://github.com/lxdvs/Volley-OkHttp-Android](https://github.com/lxdvs/Volley-OkHttp-Android)  
**Description**: 整合OkHttp和Volley。 

<a href="#networking" title="返回目录" style="width:100%"><img src="https://raw.githubusercontent.com/yeungeek/awesome-android-libraries/master/art/ic_arrow.png" align="right"/></a>
### Image Loader
#### [Cube SDK](http://cube-sdk.liaohuqiu.net/)
**Repository**: [https://github.com/etao-open-source/cube-sdk](https://github.com/etao-open-source/cube-sdk)  
**Description**: 一淘开源的一款Android开发包，包括图片加载和网络请求服务，综合了Android-Universal-Image-Loader和square等组件优点。  
**Features**:  
* 使用简单
* 加载速度快，节省资源
* 方便定制和改造
* 图片复用      
* 只关注请求结果，专注于业务
* 请求缓存 / 本地预设请求数据
* 简单的JsonData，轻松访问接口数据
* 基于Fragment的UI框架
* 屏幕尺寸信息
* 网络状态信息

#### [Glide](https://github.com/bumptech/glide)
**Repository**: [https://github.com/bumptech/glide](https://github.com/bumptech/glide)  
**Description**: 一个高效、开源、 Android设备上的媒体管理框架。灵活的API，可以和很多网络框架进行整合。    
**Features**:  
* GIF动画的解码
* 本地视频剧照的解码
* Activity生命周期的集成
* 转码的支持
* 动画的支持
* OkHttp和Volley的支持
* 其他功能：图片加载过程中占位符等

#### [ImageCache](http://www.trinea.cn/android/android-imagecache/)
**Repository**: [https://github.com/Trinea/AndroidCommon](https://github.com/Trinea/AndroidCommon)  
**Description**: Trinea开源的图片缓存，包含内存和Sdcard缓存。   
**Features**:  
*  支持预取新图片，支持等待队列
*  包含二级缓存，可自定义文件名保存规则
*  可选择多种缓存算法(FIFO、LIFO、LRU、MRU、LFU、MFU等13种)或自定义缓存算法
*  可方便的保存及初始化恢复数据
*  支持不同类型网络处理
*  可根据系统配置初始化缓存等

#### [Picasso](http://square.github.io/picasso/)
**Repository**: [https://github.com/square/picasso](https://github.com/square/picasso)  
**Description**: square开源的图片缓存。   
**Features**:   
*  可以自动检测adapter的重用并取消之前的下载
*  图片变换
*  可以加载本地资源
*  可以设置占位资源
*  支持debug模式

#### [Universal Image Loader for Android](https://github.com/nostra13/Android-Universal-Image-Loader)
**Repository**: [https://github.com/nostra13/Android-Universal-Image-Loader](https://github.com/nostra13/Android-Universal-Image-Loader)  
**Description**: 应该是使用最多的图片缓存，支持主流图片缓存的绝大多数特性。  
**Features**:   
* 多线程图片加载(同步或者异步)
* 尽可能多的配置选项（线程池，加载器，解析器，内存/磁盘缓存，显示参数等等）
* 图片可以缓存在内存中，或者设备文件目录下，或者SD卡中
* 可以监听加载进度
* 可以自定义显示每一张图片时都带不同参数
* 支持Widget  
    
**Used By**:  
[Applications using](https://github.com/nostra13/Android-Universal-Image-Loader#applications-using-universal-image-loader)

<a href="#image-loader" title="返回目录" style="width:100%"><img src="https://raw.githubusercontent.com/yeungeek/awesome-android-libraries/master/art/ic_arrow.png" align="right"/></a>

## Reference
*  [android-arsenal](https://android-arsenal.com/)
*  [Trinea android-open-project](https://github.com/Trinea/android-open-project)
*  [wasabeef awesome-android-libraries](https://github.com/wasabeef/awesome-android-libraries)

<a href="#index" title="返回目录" style="width:100%"><img src="https://raw.githubusercontent.com/yeungeek/awesome-android-libraries/master/art/ic_arrow.png" align="right"/></a>
