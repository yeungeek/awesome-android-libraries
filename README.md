# Android开源框架分类
Android开源框架库分类，挑选出最常用，最实用的开源项目，本篇主要介绍的是优秀开源框架库和项目，UI个性化控件会独立介绍。  
[UI个性化控件](https://github.com/yeungeek/awesome-android-ui)  

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/yeungeek/awesome-android-libraries?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
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
    * [Fresco](#fresco)
    * [Cube SDK](#cube-sdk)
    * [Glide](#glide)
    * [ImageCache](#imagecache)
    * [Picasso](#picasso)
    * [Universal Image Loader for Android](#universal-image-loader-for-android)
* [O/R Mapping](#or-mapping)
    * [ActiveAndroid](#activeandroid)
    * [GreenDAO](#greendao)
    * [OrmLite-Android](#ormlite-android)
    * [Realm](#realm)
    * [Sugar ORM](#sugar-orm)
* [Event Buses](#event-buses)
    * [EventBus](#eventbus)
    * [Otto](#otto)
    * [AndroidEventBus](#androideventbus)
* [JSON](#json)
    * [fastjson](#fastjson)
    * [GSON](#gson)
    * [Jackson](#Jackson)
    * [Moshi](#moshi)
* [Background Processing](#background-processing)
    * [Bolts-Android](#bolts-android)
    * [android-priority-jobqueue](#android-priority-jobqueue)
* [Image Processing](#image-processing)
    * [android-gpuimage](#android-gpuimage)
    * [ImageFilterForAndroid](#imagefilterforandroid)
* [Camera](#camera)
    * [cwac-camera](#cwac-camera)
    * [SquareCamera](#squarecamera)
    * [CameraModule](#cameramodule)
    * [OpenCamera](#opencamera)
    * [StickerCamera](#stickercamera)
* [Video](#Video)
    * [AndroidFFmpeg](#androidffmpeg)
    * [Vitamio](#vitamio)
* [Logging](#logging)
    * [Logger](#logger)
    * [DebugLog](#debuglog)
    * [hugo](#hugo)
* [Android Plugin](#android-plugin)
    * [AndroidDynamicLoader](#androiddynamicloader)
    * [dynamic-load-apk](#dynamic-load-apk)
    * [android-pluginmgr](#android-pluginmgr)
    * [DroidPlugin](#droidplugin)
* [Android Hot Fix](#android-hot-fix)
    * [Dexposed](#dexposed)
    * [AndFix](#andfix)
    * [Nuwa](#nuwa)
    * [HotFix](#hotfix)
    * [DroidFix](#droidfix)
* [Security](#security)
    * [Conceal](#conceal)
    * [SQLCipher](#sqlcipher)
* [Showcases](#showcases)
    * [PocketHub](#pockethub)
    * [iosched](#iosched)
    * [Cheesesquare](#cheesesquare)
    * [muzei](#muzei)
    * [u2020](#u2020)
* [RxJava](#rxjava)
    * [RxJava](#rxjava-1)
    * [RxAndroid](#rxandroid)
    * [RxBinding](#rxbinding)
    * [RxLifecycle](#rxlifecycle)
    * [rx-preferences](#rx-preferences)
    * [sqlbrite](#sqlbrite)    

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
[Android 三大图片缓存原理、特性对比](http://www.trinea.cn/android/android-image-cache-compare/)
#### [Fresco](http://frescolib.org/)
**Repository**:
* [https://github.com/facebook/fresco](https://github.com/facebook/fresco)  
* [http://fresco-cn.org/](http://fresco-cn.org/)  

**Description**:
Facebook 开源的一个强大的图片加载组件。  
**Features**:  
* 内存管理，两个内存缓存加上磁盘缓存构成了三级缓存
* 支持流式，图片的渐进式呈现
* 支持Gif图和WebP格式
* 更多样的显示，如圆角、进度条、点击重试、自定义对焦点
* 支持Android2.3+


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

### O/R Mapping
[5个推荐的orm框架](http://www.sitepoint.com/5-best-android-orms/)
#### [ActiveAndroid](http://www.activeandroid.com/)
**Repository**: [https://github.com/pardom/ActiveAndroid](https://github.com/pardom/ActiveAndroid)  
**Description**: ActiveAndroid是一个轻量级的orm框架，名称命令方式类似于Yii、Rails等使用的orm框架ActiveRecord。  
#### [GreenDAO](http://greendao-orm.com/)
**Repository**: [https://github.com/greenrobot/greenDAO](https://github.com/greenrobot/greenDAO)  
**Description**: GreenDAO是一个轻量级，快速的orm框架。简化建表、查询、更新、插入、事务、索引的操作。  
**Features**:
* 性能突出(比ormlite快4-5倍), [performance](http://greendao-orm.com/2011/10/23/current-performance-figures/)  
* 库小，核心包小于100k
* 简单易用的API
* 支持protobuf
* 自动生成数据库访问代码

#### [OrmLite-Android](http://ormlite.com/sqlite_java_android_orm.shtml)
**Repository**: [https://github.com/j256/ormlite-android](https://github.com/j256/ormlite-android)  
**Description**: OrmLite不是Android平台专用的orm框架，它是一个Java orm，OrmLite For Android增加了对Android平台的支持。  

#### [Realm](http://realm.io/)  
**Repository**: [https://github.com/realm/realm-java](https://github.com/realm/realm-java)  
**Description**: 移动端的数据库，适用于 Phone、Tablet、Wearable，支持 ORM，线程安全、支持连表及数据库加密，比 SQLite 性能更好。  
**Features**:
* 着重移动端
* 简单易用的API
* 支持线程安全，关系数据库和加密
* 访问快速
* 跨平台

#### [Sugar ORM](http://satyan.github.com/sugar/)  
**Repository**: [https://github.com/satyan/sugar](https://github.com/satyan/sugar)  
**Description**: Android平台专用orm框架。  
**Features**:
* 配置少
* 自动生成表结构
* 支持在不同模式版本直接切换

<a href="#or-mapping" title="返回目录" style="width:100%"><img src="https://raw.githubusercontent.com/yeungeek/awesome-android-libraries/master/art/ic_arrow.png" align="right"/></a>

### Event Buses
#### [EventBus](https://github.com/greenrobot/EventBus)
**Repository**: [https://github.com/greenrobot/EventBus](https://github.com/greenrobot/EventBus)
**Description**: 事件总线框架，非注解，效率非常高，这里是和square的otto的[对比](https://github.com/greenrobot/EventBus/blob/master/COMPARISON.md)。  
**Features**:  
* 非注解
* 便利，以onEvent方法来接收
* 性能优化，是android上最快的事件总线框架
* 单例
* 事件继承  

#### [Otto](http://square.github.io/otto/)
**Repository**: [https://github.com/square/otto](https://github.com/square/otto)  
**Description**: Square开源的事件总线框架，在Guava基础上加强，基于注解形式。

#### [AndroidEventBus](https://github.com/bboyfeiyu/AndroidEventBus)
**Repository**: [https://github.com/bboyfeiyu/AndroidEventBus](https://github.com/bboyfeiyu/AndroidEventBus)  
**Description**: [bboyfeiyu](https://github.com/bboyfeiyu)开源的事件总线框架，吸收了greenrobot的EventBus以及square的otto的优点，
并在此基础上做出了相应的改进，使得事件总线框架更适合用户的使用习惯，也使得事件的投递更加的精准、灵活。

### JSON
#### [fastjson](https://github.com/alibaba/fastjson)
**Repository**: [https://github.com/alibaba/fastjson](https://github.com/alibaba/fastjson)  
**Description**: 阿里巴巴开源JSON解析库，是一个Java语言编写的高性能功能完善的JSON库。它采用一种“假定有序快速匹配”的算法，
把JSON Parse的性能提升到极致，是目前Java语言中最快的JSON库。[各种JSON库的比较](https://github.com/alibaba/fastjson/wiki/%E5%90%84%E7%A7%8DJSON%E5%BA%93%E7%9A%84%E6%AF%94%E8%BE%83)  
**Features**:  
* 速度最快，测试表明，fastjson具有极快的性能，超越任其他的java json parser。包括自称最快的jackson
* 功能强大，完全支持java bean、集合、Map、日期、Enum，支持范型，支持自省
* 无依赖，能够直接运行在Java SE 5.0以上版本
* 支持Android

#### [GSON](https://github.com/google/gson)
**Repository**: [https://github.com/google/gson](https://github.com/google/gson)  
**Description**: google开源的JSON解析库

#### [Jackson](http://wiki.fasterxml.com/JacksonHome)
**Repository**: [https://github.com/FasterXML/jackson-core](https://github.com/FasterXML/jackson-core)  
**Description**: Jackson可以轻松的将Java对象转换成json对象和xml文档，同样也可以将json、xml转换成Java对象  

#### [Moshi](https://github.com/square/moshi)
**Repository**: [https://github.com/square/moshi](https://github.com/square/moshi)  
**Description**: square开源的JSON库，与GSON相比，更少的内建类型，更少的配置，安全的html转义等。

### Background Processing
#### [Bolts-Android](https://github.com/BoltsFramework/Bolts-Android)
**Repository**: [https://github.com/BoltsFramework/Bolts-Android](https://github.com/BoltsFramework/Bolts-Android)  
**Description**: Parse发布的面向Android的底层库集合，参见[parse-announces-bolts](http://www.infoq.com/cn/news/2014/02/parse-announces-bolts)  

#### [android-priority-jobqueue](https://github.com/path/android-priority-jobqueue)
**Repository**: [https://github.com/path/android-priority-jobqueue](https://github.com/path/android-priority-jobqueue)  
**Description**: Path开源的android优先级任务队列框架。

### Image Processing
#### [android-gpuimage](https://github.com/CyberAgent/android-gpuimage)
**Repository**: [https://github.com/path/android-priority-jobqueue](https://github.com/path/android-priority-jobqueue)  
**Description**: GPUImage是个功能十分强大、又十分易用的图像处理库。提供各种各样的图像处理滤镜，并且支持照相机和摄像机的实时滤镜。  

#### [ImageFilterForAndroid](http://www.cnblogs.com/daizhj)
**Repository**: [https://github.com/daizhenjun/ImageFilterForAndroid](https://github.com/daizhenjun/ImageFilterForAndroid)  
**Description**: 国内的代震军开源的滤镜效果框架。

### Camera
#### [cwac-camera](https://github.com/commonsguy/cwac-camera)
**Repository**: [https://github.com/commonsguy/cwac-camera](https://github.com/commonsguy/cwac-camera)  
**Description**: commonsguy开源的camera操作封装。  

#### [SquareCamera](https://github.com/boxme/SquareCamera)
**Repository**: [https://github.com/boxme/SquareCamera](https://github.com/boxme/SquareCamera)  
**Description**: 正方的摄像机，有前后摄像头等操作。  

#### [CameraModule](https://yalantis.com/?utm_source=github)
**Repository**: [https://github.com/Yalantis/CameraModule](https://github.com/Yalantis/CameraModule)  
**Description**: Yalantis开源的摄像机，有自动聚焦功能等。

#### [OpenCamera](https://github.com/almalence/OpenCamera)
**Repository**: [https://github.com/almalence/OpenCamera](https://github.com/almalence/OpenCamera)  
**Description**: 完整的摄像机，功能很全，不过代码有点乱。

#### [StickerCamera](https://github.com/Skykai521/StickerCamera)
**Repository**: [https://github.com/Skykai521/StickerCamera](https://github.com/Skykai521/StickerCamera)  
**Description**: 这是一款集成了相机,图片裁剪,给图片贴贴图打标签的相机应用。  

<a href="#camera" title="返回目录" style="width:100%"><img src="https://raw.githubusercontent.com/yeungeek/awesome-android-libraries/master/art/ic_arrow.png" align="right"/></a>

### Video
#### [AndroidFFmpeg](https://github.com/appunite/AndroidFFmpeg)
**Repository**: [https://github.com/appunite/AndroidFFmpeg](https://github.com/appunite/AndroidFFmpeg)  
**Description**: FFmpeg视频解析的例子。  

#### [Vitamio](http://www.vitamio.org)
**Repository**: [https://github.com/yixia/VitamioBundle](https://github.com/yixia/VitamioBundle)  
**Description**: Vitamio是一款Android 与iOS 平台上的全能多媒体开发框架。  
**Features**:  
* 全面支持硬件解码与 GPU 渲染
* 能够流畅播放 720P 甚至 1080P 高清 MKV，FLV，MP4，MOV，TS，RMVB 等常见格式的视频
* 在 Android 与 iOS 上跨平台支持 MMS, RTSP, RTMP, HLS(m3u8)等常见的多种视频流媒体协议，包括点播与直播

### Logging
#### [Logger](https://github.com/orhanobut/logger)
**Repository**: [https://github.com/orhanobut/logger](https://github.com/orhanobut/logger)  
**Description**: 简单、美观而且十分强大的 Android 日志工具。  

#### [DebugLog](https://github.com/MustafaFerhan/DebugLog)
**Repository**: [https://github.com/MustafaFerhan/DebugLog](https://github.com/MustafaFerhan/DebugLog)  
**Description**: 可以帮你创建更简单和更容易理解的调试日志，能够友好的显示调试信息所在类和函数。  

#### [hugo](https://github.com/JakeWharton/hugo)
**Repository**: [https://github.com/JakeWharton/hugo](https://github.com/JakeWharton/hugo)  
**Description**: 用于打印函数信息及执行时间的工具，仅在 debug 模式生效。  

### Android Plugin
#### [DynamicAPK](https://github.com/CtripMobile/DynamicAPK)  
**Repository**:  [https://github.com/CtripMobile/DynamicAPK](https://github.com/CtripMobile/DynamicAPK)   
**Description**: 实现Android多apk/dex方式的apk加载，支持资源分包。
[携程Android App插件化和动态加载实践](https://www.infoq.com/cn/articles/ctrip-android-dynamic-loading)

#### [AndroidDynamicLoader](https://github.com/mmin18/AndroidDynamicLoader)
**Repository**: [https://github.com/mmin18/AndroidDynamicLoader](https://github.com/mmin18/AndroidDynamicLoader)  
**Description**: 点评的插件化实现方式，是用 Fragment 以及 Schema 的方式实现。

#### [dynamic-load-apk](http://blog.csdn.net/singwhatiwanna/article/details/40283117)
**Repository**: [https://github.com/singwhatiwanna/dynamic-load-apk](https://github.com/singwhatiwanna/dynamic-load-apk)  
**Description**: Apk动态加载框架，热部署，利用 ClassLoader 以及 Activity 代理的方式解决。

#### [android-pluginmgr](https://github.com/houkx/android-pluginmgr)
**Repository**: [https://github.com/houkx/android-pluginmgr](https://github.com/houkx/android-pluginmgr)  
**Description**: 一种无须规范限制的动态加载解决方案，插件不需要依赖任何API  
**Features**:  
* 插件为普通apk，无须依赖任何jar
* Activity生命周期由系统自己管理
* 使用简单，只需要了解一个类PluginManager的两个方法
* 启动Activity的效率高
* 不修改插件，被加载的插件仍然可以独立安装。

#### [DroidPlugin](https://github.com/Qihoo360/DroidPlugin)
**Repository**: [https://github.com/Qihoo360/DroidPlugin](https://github.com/Qihoo360/DroidPlugin)  
**Description**: DroidPlugin 是360手机助手在Android系统上实现了一种新的插件机制:它可以在无需安装、修改的情况下运行APK文件,此机制对改进大型APP的架构，实现多团队协作开发具有一定的好处。  
**Features**:  
* 支持Androd 2.3以上系统
* 插件APK完全不需做任何修改，可以独立安装运行、也可以做插件运行。要以插件模式运行某个APK，你无需重新编译、无需知道其源码。
* 插件的四大组件完全不需要在Host程序中注册，支持Service、Activity、BroadcastReceiver、ContentProvider四大组件
* 插件之间、Host程序与插件之间会互相认为对方已经"安装"在系统上了。
* API低侵入性：极少的API。HOST程序只是需要一行代码即可集成Droid Plugin
* 超强隔离：插件之间、插件与Host之间完全的代码级别的隔离：不能互相调用对方的代码。通讯只能使用Android系统级别的通讯方法。
* 支持所有系统API
* 资源完全隔离：插件之间、与Host之间实现了资源完全隔离，不会出现资源窜用的情况。
* 实现了进程管理，插件的空进程会被及时回收，占用内存低。
* 插件的静态广播会被当作动态处理，如果插件没有运行（即没有插件进程运行），其静态广播也永远不回被触发。  

_限制和缺陷:_
* 无法在插件中发送具有自定义资源的Notification，例如： a. 带自定义RemoteLayout的Notification b. 图标通过R.drawable.XXX指定的通知（插件系统会自动将其转化为Bitmap）
无法在插件中注册一些具有特殊Intent Filter的Service、Activity、BroadcastReceiver、ContentProvider等组件以供Android系统、已经安装的其他APP调用。
* 对Activity的LaunchMode支持不够好，Activity Stack管理存在一定缺陷。Activity的onNewIntent函数可能不会被触发。 （此为BUG，未来会修复）
缺乏对Native层的Hook，对某些带native代码的apk支持不好，可能无法运行。比如一部分游戏无法当作插件运行。

### Android Hot Fix
> 参考 [各大热补丁方案分析和比较](http://blog.zhaiyifan.cn/2015/11/20/HotPatchCompare/)

#### [Dexposed](https://github.com/alibaba/dexposed)
**Description**: 基于[Xposed](https://github.com/rovo89/Xposed)的AOP框架，方法级粒度，可以进行AOP编程、插桩、热补丁、SDK hook等功能。

#### [AndFix](https://github.com/alibaba/AndFix)
**Description**: 阿里巴巴的另一个团队的hot fix方案。同样是方法的hook，AndFix不像Dexposed从Method入手，而是以Field为切入点。

>下面的几种是基于[ClassLoader](http://bugly.qq.com/blog/?p=781)机制来实现hot fix方案。是原腾讯空间Android工程师，陈钟发明的热补丁方案，是他在看源码的时候偶然发现的切入点。

#### [Nuwa](https://github.com/jasonross/Nuwa)
**Description**: 纯java实现的hot fix方案  
**Features**:
* Support both dalvik and art runtime.
* Support productFlavor and buildType.
* Support proguard and multidex.
* Pure java implementation.

#### [HotFix](https://github.com/dodola/HotFix)
**Description**: 安卓App热补丁动态修复框架  

#### [DroidFix](https://github.com/bunnyblue/DroidFix)
**Description**: AndroidHotFix/Android 代码热修复  

> 比较：  
> 1. Dexposed不支持Art模式(5.0+)  
> 2. AndFix支持2.3-6.0  
> 3. ClassLoader方案支持2.3-6.0    
> 在兼容性稳定性上，ClassLoader方案很可靠，如果需要应用不重启就能修复，而且方法足够简单，可以使用AndFix，而Dexposed由于还不能支持art

### Security
#### [Conceal](http://facebook.github.io/conceal/)
**Repository**: [https://github.com/facebook/conceal](https://github.com/facebook/conceal)  
**Description**: Conceal是一套用于Android上的文件加密和鉴权的Java API

#### [SQLCipher](https://www.zetetic.net/sqlcipher/sqlcipher-for-android/)
**Repository**: [https://github.com/sqlcipher/android-database-sqlcipher](https://github.com/sqlcipher/android-database-sqlcipher)  
**Description**: Sqlite 加密工具

### Showcases
#### [PocketHub](https://github.com/pockethub/PocketHub)
**Repository**: [https://github.com/pockethub/PocketHub](https://github.com/pockethub/PocketHub)  
**Description**: Github 的 Android 客户端项目

#### [iosched](https://github.com/google/iosched)
**Repository**: [https://github.com/google/iosched](https://github.com/google/iosched)  
**Description**: The Google I/O 2014 Android App

#### [Cheesesquare](https://github.com/chrisbanes/cheesesquare)
**Repository**: [https://github.com/chrisbanes/cheesesquare](https://github.com/chrisbanes/cheesesquare)  
**Description**: Demos the new Android Design library

#### [muzei](http://muzei.co/)
**Repository**: [https://github.com/romannurik/muzei](https://github.com/romannurik/muzei)  
**Description**: 定时更换桌面精美壁纸

#### [u2020](https://github.com/JakeWharton/u2020)
**Repository**: [https://github.com/JakeWharton/u2020](https://github.com/JakeWharton/u2020)  
**Description**: 开源框架集成的demo

### RxJava
> Reactive Extensions for the JVM – a library for composing asynchronous and event-based programs using observable sequences for the Java VM

这是RxJava在github上的描述，它是响应式编程在JVM上的一个扩展，核心在于异步。那对于Android来说，带来了什么。
具体的可以看看[扔物线](https://github.com/rengwuxian)写的[给 Android 开发者的 RxJava 详解](http://gank.io/post/560e15be2dca930e00da1083)，非常的详细，该有的都有。下面的是一些RxJava的延伸。

#### [RxJava](https://github.com/ReactiveX/RxJava)
这是本尊，基类，下面的库都是基于RxJava。

#### [RxAndroid](https://github.com/ReactiveX/RxAndroid)
RxJava在Android的扩展，从版本0.25升级到1.x后，改变非常大，现在1.x剩下来的就只有[AndroidSchedulers](https://github.com/ReactiveX/RxAndroid/blob/master/rxandroid%2Fsrc%2Fmain%2Fjava%2Frx%2Fandroid%2Fschedulers%2FAndroidSchedulers.java)。从中剥离出来[RxBinding](https://github.com/JakeWharton/RxBinding),[RxLifecycle](https://github.com/trello/RxLifecycle),[rx-preferences](https://github.com/f2prateek/rx-preferences)等，详细请看[How to upgrade to RxAndroid 1.0](http://blog.danlew.net/2015/09/01/how-to-upgrade-to-rxandroid-10/)

#### [RxBinding](https://github.com/JakeWharton/RxBinding)
Jake大神的作品，UI控件的RxJava实现

#### [RxLifecycle](https://github.com/trello/RxLifecycle)
RxAndroid的生命周期控制

#### [rx-preferences](https://github.com/f2prateek/rx-preferences)
SharedPreferences的实现

#### [sqlbrite](https://github.com/square/sqlbrite)
android sqlite的实现

<a href="#index" title="返回目录" style="width:100%"><img src="https://raw.githubusercontent.com/yeungeek/awesome-android-libraries/master/art/ic_arrow.png" align="right"/></a>

## Reference
*  [android-arsenal](https://android-arsenal.com/)
*  [Trinea android-open-project](https://github.com/Trinea/android-open-project)
*  [wasabeef awesome-android-libraries](https://github.com/wasabeef/awesome-android-libraries)
