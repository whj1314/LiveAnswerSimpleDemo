# LiveAnswerSimpleDemo

基于环信开发在线直播答题开源项目

## 1 项目初衷

2018年伊始，全民直播答题浪潮来袭，一度被认为是一个新的互联网风口，王思聪凭借在现象级产品《冲顶大会》上疯狂"撒币"一时风光无二，凭借超高奖金和超低门槛吸引了大量网民参与和市场的目光。正因为直播答题是一种通过极低的成本来推动APP获客、保留存、拉活跃的新模式，各类直播答题APP如雨后春笋般进入大家的视野，越来越多企业希望赶上这波风口，快速搭建一套直播答题系统。作为一名环信生态圈资深开发者，本着对技术的热衷，对环信的眷恋和对党的忠诚，基于环信即时通讯云写了“小信竞答”这个直播答题开源项目，目前项目源码已全部免费开放，希望对有需求的企业和开发者提供一个思路和参考。
## 2 方案架构

![](https://github.com/LijieSong/LiveAnswerSimpleDemo/blob/master/img/theFlowChart.png)

## 3 功能介绍

整个项目分为管理员端，观众端和服务端，首先在服务端预设好题目，由管理员发起直播开始答题，服务端收到指令将12道题目利用环信IM推送到观众端，观众端收到题目开始答题，将答案返回给服务端由服务端进行判断，如果答题正确进入下一题，答题错误判断是否使用复活卡，这里要注意的是需要加一个复活卡的使用次数判断。

   在整个答题过程中，管理员端会定时去服务端查询答题结果，等到全部答题结束，点击结束本次答题，服务端将计算好的结果返回并发放奖金，使用环信IM推送将答题结果推给观众端。

![](http://www.imgeek.org/uploads/article/20180316/32eda3cc6c871d984ddcbe6a808fc6b8.jpg)
## 4 关于直播间
      直播间由直播画面和聊天室两个部分组成，“小信竞答”的聊天室使用环信聊天室，集成比较简单，基础版就能支持5000人在线聊天，增值服务版聊天室人数无上限，可以去环信官网注册一个开发者账号，创建应用将APPKEY替换成自己的；环信直播聊天室可以集成所有市场主流CDN厂商的推拉流功能(腾讯，七牛，UCloud，网宿等)。

环信直播聊天室特点 
This is Title
1、采用支持高并发的异步架构，轻松应对千万级并发请求; 各项基础服务集群化，确保系统高可用性; 系统冗余度高，容量评估体系完善，弹性扩容应对流量峰值；
2、支持各种消息格式：文字、表情、图片、声音、视频、附件、位置、扩展消息；
3、支持实时配置的消息分级策略，确保重要消息优先必达； 
4、支持直播聊天室后台管理及审核功能，提供直播相关数据统计；
5、提供智能反垃圾和自定义敏感词过滤功能；
6、快速集成，demo提供高质量代码示例，可根据运营情况随时扩展；
7、聊天室人数无上限
### 写在最后
  小信竞答源码全部开放，仅供学习和参考，如果作为商业用途，按照广电总局对网络直播答题节目管理的，需要 “网络视听许可证、主持人持证、还有通过审批发放的节目备案号”，三证缺一不可，未持有《信息网络传播视听节目许可证》的任何机构和个人，一律不得开办网络直播答题节目。

本月底《环信公开课第19期-直播答题开源项目》将线上讲解“小信竞答”实现思路，手把手教您从零开始搭建一个直播答题项目，扫码加入公开课微信群与大牛面对面交流。

![](http://www.imgeek.org/uploads/article/20180316/406a306baa734198988ab2b2818309a0.jpg)

