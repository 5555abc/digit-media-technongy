-----

> markdown语法进阶
>
> 1.代码块
>
> ```css
> print（“hello world”）
> ```
>
> ```css
> <!DOCTYPE html>
> <html>  
> <head>
> <meta charset="utf-8"> 
>   <title >断字</title>
>   <style>p.test{ width:11em;border:1px solid
>       #000000;}
> 
>     h1{
>   text-shadow: 5px 5px 5px #FF0000;
> }
>   </style>
>   
>   </head>
>     <body>
>       <h1>Text-shadow effect!</h1>
>       <p class="test">
>  下表列出了所有 CSS3 的多列属性：
> 
> 
> column-count      指定元素应该被分割的列数。
> column-fill       指定如何填充列
> column-gap        指定列与列之间的间隙
> column-rule       所有 column-rule-* 属性的简写
> column-rule-color 指定两列间边框的颜色
> column-rule-style 指定两列间边框的样式
> column-rule-width 指定两列间边框的厚度
> column-span       指定元素要跨越多少列
> column-width      指定列的宽度
> columns column-width 与 column-count 的简写属性。
>       </p>
>     
>     
> </body>
> </html>
> ```
>
> 2.流程图
>
> > ```mermaid
> > graph TB
> > A[Apple]-->B{Boy}
> > A---C(Cat)
> > B.->D((Dog))
> > C==喵==>D
> > style A fill:#2ff,fill-opacity:0.1,stroke:#faa,stroke-width:3px
> > style D stroke:#000,stroke-width:8px
> > 
> > ```

# 显示方向

- TB/TD(top bottom/top down)表示从上到下

- BT （bottom top)表示从下到上

- RL（right left）表示从右到左

- LR（letf right)表示从左到右

  ### 节点类型

    <font color=Blue> 节点本身的展现形式，是通过不同括号来代表各自不同的形状，默认为矩形。</font>
  
  - 默认节点： A
  - 矩形节点： B[矩形]
  - 圆角矩形节点： C(圆角矩形)
  - 圆形节点： D((圆形))
  - 非对称节点： E>非对称]
  - 菱形节点： F{菱形}
  
  ## 插入图片
  
  ![file:///C:/Users/pipi%E7%9A%AE%E5%8D%A1%E4%B8%98/Desktop/css/QQ%E5%9B%BE%E7%89%8720211109084329.png](C:\Users\pipi皮卡丘\Desktop\css\QQ图片20211109084329.png)

> - 实践1：flowchart流程图
>
> > **牢记tag=>type: content:>url**
>
> ![微信图片_20211110212828](C:\Users\pipi皮卡丘\Desktop\css\微信图片_20211110212828.png)
>
> ```flow
> st=>start: Start|past:>http://www.baidu.com
> e=>end: End:>http://www.baidu.com
> op1=>operation: My Operation|past
> op2=>operation: Stuff|current
> sub1=>subroutine: My Subroutine|invalid
> cond=>condition: Yes or No?|approved:>http://www.baidu.com
> c2=>condition: Good idea|rejected
> io=>inputoutput: catch something...|request
> 
> st->op1(right)->cond
> cond(yes, right)->c2
> cond(no)->sub1(left)->op1
> c2(yes)->io->e
> c2(no)->op2->e
> ```
>
> 
>
> - 实践2：网新专业培养方案
>
>   > ```mermaid
>   > graph LR
>   > 1[TREE]-->2(融合新闻学)
>   > 1-->3(网页设计与制作)
>   > 1-->4(数字媒体技术)
>   > 2-->6(数字多媒体技术)
>   > 2-->5(新闻传播与研究方法)
>   > 3-->7(电子商务基础与应用)
>   > 3-->17(H5互动技术与应用)
>   > 4-->8(python语言)
>   > 5-->9(大数据)
>   > 7-->9(大数据)
>   > 8-->10(API,机器学习与人工智能)
>   > 8-->16(web数据挖掘)
>   > 8-->11(网络舆情监测与研判)
>   > 9-->12(互交技术)
>   > 9-->13(网站运营与管理)
>   > 9-->14(新媒体产品设计与项目管理)
>   > 9-->15(信息可视化)
>   > 10-->14(新媒体产品设计与项目管理)
>   > 10-->21(python数据分析)
>   > 10-->21(移动互联网开发)
>   > 12-->18(用户分析)
>   > 13-->19(能力培养)
>   > 14-->19(能力培养)
>   > 16-->20(python数据分析)
>   > 17-->21(移动互联网开发)
>   > 17-->22(前端开发框架)
>   > 18-->23(产品策划运营)
>   > 18-->24(社会数据科学)
>   > 19-->25(写作练习)
>   > 20-->28(新媒体数据分析与应用)
>   > 20-->29(互交设计与前端设计)
>   > 20-->30(用户研究与数据分析)
>   > 21-->28(新媒体数据分析与应用)
>   > 21-->29(互交设计与前端设计)
>   > 22-->28(新媒体数据分析与应用)
>   > 25-->26(文献总数与写作)
>   > 25-->27(实践社群与自我策展)
>   > 28-->25(写作训练)
>   > 29-->31(微信小程序开发与运营)
>   > 30-->32(数据产品经理/平台型产品经理/产品体验设计)
>   > 
>   > 
>   > 
>   > 
>   > 
>   > style 1 fill:yellow
>   > style 2 fill:yellow
>   > style 3 fill:yellow
>   > style 4 fill:yellow
>   > style 5 fill:yellow
>   > style 6 fill:yellow
>   > style 7 fill:yellow
>   > style 8 fill:yellow
>   > style 10 fill:yellow
>   > style 11 fill:yellow
>   > style 9 fill:green
>   > style 12 fill:green
>   > style 13 fill:green
>   > style 14 fill:green
>   > style 15 fill:green
>   > style 18 fill:green
>   > style 19 fill:green
>   > style 23 fill:green
>   > style 24 fill:green
>   > style 16 fill:red
>   > style 17 fill:red
>   > style 20 fill:red
>   > style 21 fill:red
>   > style 22 fill:red
>   > style 28 fill:red
>   > style 25 fill:pink
>   > style 26 fill:blue
>   > style 27 fill:blue
>   > style 29 fill:purple
>   > style 30 fill:purple
>   > style 31 fill:purple
>   > style 32 fill:purple
>   > 
>   > 
>   > ```
>   >
>   > 
>
> 

> - 实践3：甘特图
>
> > ```mermaid
>> gantt
> > dateFormat YYYY-MM-DD
> > TITLE 产品计划表
> > section 阶段一
> > 产品原型图:2021-11-11,2021-11-20
> > section 阶段二
> > 产品交互图:2021-11-22,2021-12-10
> > section 阶段三
> > 前端开发:2021-12-19,2021-12-26
> > 
> > 
> > 
> > 
> > ```

![微信图片_20211110200717](C:\Users\pipi皮卡丘\Desktop\css\微信图片_20211110200717.png)

 
