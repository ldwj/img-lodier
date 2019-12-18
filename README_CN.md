# 本demo示例主要作为演示demo使用，目前包含常用工具库、Xutil网络访问库、日期选择库、Tab样式、zXing二维码的生成和扫描库等，下面一一做详细介绍

## libraryApplication application基础库
#### 描述: 
         本基础库就一个application,为的就是外部调用的使用不需要再传输Content,直接集成该库，调用BaseApplication.getInstance()
**引用的三方库明细**
* com.android.support:multidex:1.0.3 分包库

**引用方式**
* 在最外层中引用仓库地址


![引用示例图片](https://raw.githubusercontent.com/ldwj/img-lodier/master/image2.png) 
 ```
        maven(){url 'http://192.168.240.114:8081/nexus/content/repositories/library_application/'}
 ```
* 在需要的model中引用一下库即可使用，注意版本号的更新
 ```
        implementation 'com.tiamaes.android.library:library_application:1.0.0'
 ```
 
 
## libraryUtil 工具库
#### 描述: 
          本库主要列举了一些常用的方法，重写的基础组件等


**引用的三方库明细**
* com.android.support:appcompat-v7:28.0.0
* libraryApplication

**引用方式**
* 在最外层中引用仓库地址
 ```
        maven(){url 'http://192.168.240.114:8081/nexus/content/repositories/library_util/'}
 ```
* 在需要的model中引用一下库即可使用，注意版本号的更新
 ```
        implementation 'com.tiamaes.android.library:library_util:1.0.1'
 ```

**包含的工具类说明**

文件名称|说明 |包含方法
----|-----|------
AdapterBase|ListView的适配器基类|
AppManager|activity统一管理|添加、删除单个、删除全部、保留某个删除其余的全部
AppUtil|常用工具类|判断网络、获取程序的版本信息、获取imei等
CacheUtils|缓存工具类|缓存字符、json、实体对象、bitmap、Drawable等，计算缓存大小、清空缓存、删除缓存目录
DateTimeUitl|时间格式化工具类|对时间格式化、转换等操作
FileUtil|文件处理工具类|对文件、文件夹等判断、新增、删除、复制、重命名、压缩、解压等操作
ImgBitmapUtil|Bitmap处理工具类|创建倒影图片、圆角、方角处理、旋转、模糊、添加边框、view保存成图片到相册并更新、获取View的bitmap
IntentUtils|意图相关工具类|卸载、安装、分享、打开相册等意图
LatLon2LatlonUtil|坐标转换|高德、百度、火星坐标等之间的相互转换
PakageInfoUtil|系统安装应用相关|获取相同安装的应用、过滤三方应用
PinyinUtils|拼音相关工具类|汉字转拼音、获取第一个汉字、所有汉字的首字母、根据名字获取姓氏拼音等
ScreenUtils|屏幕相关辅助类|获取屏幕宽、高，状态栏的高度、dp与px的转换
SharedPreferencesUtils|sp缓存|字符、booble、int等的存储和读取
StringUtils|字符串处理工具类|判断字符是否为空、手机号、邮箱、身份证的校验、是否包含中文、数字、是否是日期格式、获取地区编码、String与double、int之间的转换（含有保留小数）、获取textView最多展示多少个字、字符转与ASCII码的转换、进制之间的转换
TMLogUtil|日志打印工具类|log日志打印，包含是否打印日志、打印日志的Tag设置、i、d、e、v、w等级别
ToastUtils|文本弹出工具类|弹出文本提醒，可设置弹出文本的时间长短、位置等
WordReplacement|输入密码时出现短暂明文问题|配合EditText输入密码时出现短暂明文的解决，详情用法参考示例demo

**重写的自定义插件**

文件名称|说明 |
----|-----|
CircleProgressView|开锁执行动画效果
CircularImage|自定义圆形图片
ClearEditText|带有删除按钮的输入框
DrawableCenterTextView|drawableLeft与文本一起居中显示
MultiStateView|通过设置状态展示不同的view
MyGridView|适配ScrollView滑动
MyListView|适配ScrollView滑动
NumberInputView|自定义输入验证码数字框
SwipeMenuLayout|侧滑菜单，可自定义滑出内容
treelist|无线循环的自定义树形架构，详情参考用例(目前是全部选择子之后，父才会被选中，如果想实现选中子之后，父的状态也有变化，联系李丹，有现成的用例)
stepview|仿物流详情信息的框架，具体用法参考用例25
flippingloadingdialog|自定义Loading框
shapeload|自定义Loading框



## libraryXutil 网络访问库
#### 描述: 
          本库主要封装了Xutil的网络访问
          
**引用的三方库明细**
* org.xutils:xutils:3.5.0
* com.google.code.gson:gson:2.8.5
* libraryApplication

**引用方式**
* 在最外层中引用仓库地址
 ```
        maven(){url 'http://192.168.240.114:8081/nexus/content/repositories/library_xutils/'}
 ```
* 在需要的model中引用一下库即可使用，注意版本号的更新
 ```
        implementation 'com.tiamaes.android.library:library_xutils:1.0.1'
 ```


**包含的工具类说明**

文件名称|说明 |包含方法
----|-----|------
HttpUtils|网络访问对外方法类|直接调用该方法POST\GET\DELETE等方法(如果需要在Header中添加信息，可自定义RequestParams添加)


## librarypulltorefresh 下拉刷新、上拉加载库
#### 描述: 
          本库主要封装了可下拉刷新的自定义组件
          
**引用的三方库明细**
 无
 
 
 **引用方式**
* 在最外层中引用仓库地址
 ```
        maven(){url 'http://192.168.240.114:8081/nexus/content/repositories/library_listview/'}
 ```
* 在需要的model中引用一下库即可使用，注意版本号的更新
 ```
        implementation 'com.tiamaes.android.library:library_listview:1.0.0'
 ```

**包含的工具类说明**

文件名称|说明 
----|-----
PullToRefreshExpandableListView|下拉加载、上拉刷新的ExpandableListView
PullToRefreshGridView|下拉加载、上拉刷新的GridView
PullToRefreshHorizontalScrollView|下拉加载、上拉刷新的横向ScrollView
PullToRefreshListView|下拉加载、上拉刷新的横向ListView
PullToRefreshScrollView|下拉加载、上拉刷新的横向ScrollView
PullToRefreshWebView|下拉加载、上拉刷新的横向WebView

* 具体使用方法参考用例



## libraryPickerview 日期选择库
#### 描述: 
          本库主要封装了日期的选择、地区的选择、自定义选择样式等，可设置选择日期的格式，可单独设置选择年、月、日、时、分、秒的任何一种（具体使用方法参考用例tm026）
也可以参考官方说明链接：           
[Pickerview官方说明](https://github.com/Bigkoo/Android-PickerView/blob/master/README.md)          

**引用的三方库明细**
* com.android.support:support-annotations:28.0.0

**引用方式**
* 在最外层中引用仓库地址
 ```
        maven(){url 'http://192.168.240.114:8081/nexus/content/repositories/library_picker_view/'}
 ```
* 在需要的model中引用一下库即可使用，注意版本号的更新
 ```
        implementation 'com.tiamaes.android.library:library_picker_view:1.0.0'
 ```

## libraryTabLayout 日期选择库
#### 描述: 
          本库主要封装了常用Tab的用法，根据属性设置展示位置、背景颜色、字体颜色、选中的颜色，可左右滑动等，具体参考示例tm022
          
也可以参考官方说明链接：           
[TabLayout官方说明](https://github.com/wf864617223/FlycoTabLayout-master/blob/master/README_CN.md)
          
**引用的三方库明细**
* com.android.support:support-v4:25.2.0


**引用方式**
* 在最外层中引用仓库地址
 ```
         maven(){url 'http://192.168.240.114:8081/nexus/content/repositories/library_tab_layout/'}
 ```
* 在需要的model中引用一下库即可使用，注意版本号的更新
 ```
        implementation 'com.tiamaes.android.library:library_tab_layout:1.0.0'
 ```


