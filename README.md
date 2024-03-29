# 博物馆PRD文档
************
## PRD价值主张设计
### PRD加值宣言（使用场景）
* 目标用户：来博物馆的游客以及科研人员
* 功能使用场景描述：

（1）游客来到博物馆，在欣赏展品时，不想阅读文字，可使用博物馆app进行智能语音交互将文字转为语音。

（2）当外国游客来到博物馆，对馆内的中英文提示都无法理解时，可使用博物馆的APP进行机器翻译。

（3）当用户在逛纪念品店，想找到某一款商品同款或相似的商品，不用一件件的看，可使用博物馆app进行图像搜索，找到同样或相似的商品并找到商品相应位置及相关信息。

****************
### 核心价值
* 本APP（小程序）旨在通过整合各种API，使它们组合起来发挥出更大的作用，进而方便游客解决在参观中遇到的问题。

### 核心价值与用户痛点
* 我们使用阿里的语音交互API及地图API，将展品的介绍以语音形式播放给用户（需要佩戴耳机），更好的分配了游客的听觉和视觉。使游客参观过程中可以不用阅读大量的文字信息，注重在展品本身。同时还具有语音问答功能，用户可以向该软件提问，例如：怎么走到3号展馆？能向我介绍一下编号xxx的展品吗？等等。

* APP的云端服务器内储存了该博物馆的所有展品图片及信息，我们利用图像识别API，给用户一个更好的搜索方式。用户有多种方式来找到目标展品，一是基本搜索，在APP现有的数据中搜索，二是对着展品或者展品海报拍照，使用图像识别API来对比数据库内的展品，得出的结果以相似度从高至低排列。从而得知目标展品位置，配合地图API进行语音导航。

* 整个APP都可以随时调用翻译API，默认语言是手机系统语言，如需要显示默认语言或翻译成其他语言，只需要长按文字就可进行翻译。

### 人工智能概率性
1. 图像搜索有概率会因为用户拍照的角度不同或者光泽、像素不同导致返回的结果不同，从何影响到用户的体验。
2. 机器翻译同样可能会出现概率失误，从而影响解决用户痛点。

### 需求列表与人工智能API加值
|需求 |API |
|:---:|:---:|
|参观者想方便找到自己所想看的文物位置 |图像识别 |
|外宾了解文物介绍，解决语言障碍的问题|机器翻译|

***************
## 原型设计
### 功能一：展品介绍及寻找
>用户使用APP上传展品图片，会自动生成当前位置到该展品的介绍和地图线路。查看展品介绍和地图线路。。
![232517_e36c4797_1648154.png](https://upload-images.jianshu.io/upload_images/9860856-0a03d11523ac00e5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


### 功能二：翻译
>用户在使用app进行操作到信息内容页面后header部分会有语言栏进行语言选择，用户可以根据自己的需求选择语言，页面会根据选择的语言进行翻译。
![232547_50e8a573_1648154.jpeg](https://upload-images.jianshu.io/upload_images/9860856-a267a8c21dc8bdf1.jpeg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


### 功能三：语音交互
>用户打开智能语音交互界面，用语音的形式提出问题，APP会识别用户提出的问题，同时反馈相关的回答内容。
![232616_3f968ece_1648154.jpeg](https://upload-images.jianshu.io/upload_images/9860856-00b7d069def695e1.jpeg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


### APP上的体现
* 用于进入APP主界面，通过点击“展品介绍及寻找”和“智能语音问答”按钮可以实现不同功能：

* 1.首先点击“展品介绍及寻找”按钮进入对应界面。用户通过上传展品图片来实现“展品介绍和寻找”功能；点击header可实现“翻译”功能。

* 2.再点击“智能语音问答”按钮，用户进入问答界面，用户可通过发送语音获得信息的形式实现“智能语音问答”的功能。
![232735_55d0f32e_1648154.png](https://upload-images.jianshu.io/upload_images/9860856-cbc1d185c4086137.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

********************


