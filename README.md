# LayoutTest
Layout相关的一些要点
=====
每个layout都是 viewGroup的子类，每个layout都有自己nested的LayoutParams
Linearlayout:
------
常用的属性有 gravity 后缀:gravity都是表示对齐方式的属性（alignment）其中gravity是表示该view中的内容的对齐方式，layout_gravity表示该view在parent中的对齐方式  
android:gravity - Controls the alignment of the view content (akin to text-align in CSS)  
android:layout_gravity - Controls the alignment of the view within it's parent container (akin to float in CSS)  
android:layout_weight - Specifies how much of the extra space in the layout to be allocated to a view  
RelativeLayout
------
RelativeLayout positions views based on a number of directional attributes:  
Position based on siblings: layout_above, layout_below, layout_toLeftOf, layout_toRightOf  
Position based on parent: layout_alignParentTop, layout_alignParentBottom, layout_alignParentLeft, layout_alignParentRight, android:layout_centerHorizontal, android:layout_centerVertical  
Alignment based on siblings: layout_alignTop, layout_alignBottom, layout_alignLeft, layout_alignRight, layout_alignBaseline  
对于垂直上,layout_alignLeft跟layout_alignRight可以控制width  
对于水平上，layout_alignTop 跟layout_alignBottom可以控制height  
PercentRealtviewLayout 
------
目前google推出了两种百分比的layout，PercentRelativeLayot和PercentFrameLayout，支持的属性有    
layout_widthPercent、layout_heightPercent、 layout_marginPercent、layout_marginLeftPercent、   
layout_marginTopPercent、layout_marginRightPercent、layout_marginBottomPercent、  
layout_marginStartPercent、layout_marginEndPercent。  
可以看到支持宽高，以及margin。  
我们只要在开发过程中使用PercentRelativeLayout、PercentFrameLayout替换FrameLayout、RelativeLayout即可。别忘了添加依赖compile 'com.android.support:percent:23.0.0'  
FramLayout
------
frameLayout中后来的子View会绘制在之前的view之上，就像一个栈。通过layout_gravity配合上padding或margin可以来安排子view在framelayou中的位置。  
the last child added to a FrameLayout will be drawn on top of all the previous children. Think of it like a   stack of items, the item last put on the stack will be drawn on top of the items below it. This layout makes   it very easy to draw on top of other layouts, especially for tasks such as button placement.   
To arrange the children inside of a FrameLayout use the android:gravity attribute along with whatever android:paddingand android:margin you need.  
 
