# LanSoEditor_advance
android  video editor  advance sdk . filter, overlay,remark,mixer and so on安卓平台视频编辑高级版本，可以滤镜，叠加，标记等操作
####工程为Eclipse,修改为Android Studio的步骤
*  选择AS中的file--->import project ,选择项目的路径名，（注意，一定要是当前项目的根文件夹），点击Ok，会弹出对话框，让您选择需要保存的路径， 选择后点击Next,会弹出3个按钮都选中的对话框，直接点击Finish，导入完成。
*  可联系我们,为您转换成Android Studio版本工程, 并提供技术支持(联系方式见下面). 

###当前版本是LanSoEditor_advance1.9.0 视频编辑的高级版本
*  基本覆盖了秒拍,美拍,快手等视频编辑的大部分功能.
*  采用全新的[画板]+ [画笔] 的编程思想.
*  增加了44种滤镜,基本覆盖市面上大部分APP中的滤镜效果.
*  可以实现视频和视频, 视频和图片,视频和您的UI界面叠加.
*  在叠加的过程中:支持任意时间点的加入,隐藏,显示,退出.支持同时获取媒体来任意叠加,支持叠加过程中的各种调节,支持实时保存.
*  可以实现 图片和图片的叠加,来实现多张图片合并成影集的效果.
*  可以实现涂鸦, 浪漫情诗等效果.
*  我们完全以API的形式呈现,稳定可靠,简单易用,您可以根据项目的个性化而任意的发挥.


###核心架构
*  我们设计了Pen类,可以实现旋转,缩放,平移,RGBA值的调节,隐藏/显示等功能,您可以认为类似Android的各种控件继承自View一样使用.
*
*  我们设计了DrawPad架构, 他是一个画板, 您可以在上面增加一个画笔或多个画笔.获取一个Pen(画笔),释放一个Pen(画笔).
*  
*  当前继承Pen的有:VideoPen,BitmapPen,FilterPen,ViewPen; 
*  VideoPen: 处理视频画面,可以从DrawPad"媒体池"中获取多个,从中得到surface,设置到您的播放器中,然后在播放过程中进行各种编辑功能,
								比如您可以同时获取两个VideoPen,一个用来显示,另一个把透明度调整为0来叠加,实现透明叠加的效果								
								
*  FilterPen: 处理视频滤镜,同VideoPen一样使用,并支持44种视频滤镜,您可以在视频播放中,任意的更换滤镜效果,
									也可以在滤镜过程中增加另外的IPen,一起实现您的个性化效果.
									
*  BitmapPen: 处理图片画面,可以从DrawPad"媒体池"中获取多个,可以单独使用,来生成照片影集,也可以和别的IPen混合使用,呈现花样的效果.

*  ViewPen  : 处理您设计的UI,比如你可以关联一个TextView,把TextView上的文字加到视频中,也可以关联一个您设计好的炫酷的UI效果,
								比如一个LinearLayout,一个RelativeLayout等等.							来合成视频,这个我们后期会陆续的增加各种举例,当然您也可以自由发挥.			
* CanvasPen  :  传递一个Canvas对象给您, 您可以在上面绘制各种Canvas的方法,不同于ViewPen,可前台/也可后台.
* MVPen      :   负责绘制各种MV动画,比如画板上已有视频，则等于在视频上增加MV效果
* StickerPen :		负责绘制各种动态贴纸到画板上，综艺节目中后期加的大多是这个。
											
*  此SDK采用为收费授权,公司性质的合作,为了您项目更好的进行,欢迎和我们联系.谢谢!

###更仅一步说:
*	1，你用 【视频画笔 VideoPen】在 画板 DrawPad上作画， 就得到 调整后的视频

* 2，你用  【图片画笔 BitmapPen】在画板上作画， 就得到 动态的照片影集。

*	3，你用 【UI画笔  ViewPen】在画板上作画， 就是把精美的UI界面转换为视频， 当然我们的设计，也可以后台处理。

* 4， 你用 【视频画笔】+ 【图片画笔】 在画板上作画， 就得到动态的视频图片效果。

* 5， 你用  【视频画笔】 + 【MV画笔】 在画板上作画， 就是在视频中叠加MV的效果。

* 6， 当然： 画板 可以在前台工作， 也可以在后台处理。



###下载地址: 
*  https://github.com/LanSoSdk/LanSoEditor_advance

###我们有基本视频编辑,以方便您项目中基本需求：
*	https://github.com/LanSoSdk/LanSoEditor_common


###直接下载获取APK:
   下载整个项目后, 在bin文件下有apk, 直接安装后即可演示.


###联系方式:
*   QQ 1852600324 
*   Email:support@lansongtech.com
