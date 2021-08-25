# 工作常用好用的网址

1. [https://wordhtml.com/](https://wordhtml.com/) 使用场景：用户协议，隐私协议等。纯文本的页面，可直接在该网址转换成HTML页面。
2. 压缩图片 [https://tinyjpg.com/](https://tinyjpg.com/)
3. 将网址转换成二维码图片 [https://www.qr-code-generator.com/](https://www.qr-code-generator.com/)
4. 将二维码图片解码，看URL路径 [https://jiema.wwei.cn/](https://jiema.wwei.cn/)
5. Json格式化校验 [https://www.bejson.com/json/format/](https://www.bejson.com/json/format/)
6. 日期格式化 [http://momentjs.cn/](http://momentjs.cn/)
7. 扩展程序[chrome://extensions/](chrome://extensions/)
8. 时间戳，日期格式相互转换 [https://www.beijing-time.org/shijianchuo/](https://www.beijing-time.org/shijianchuo/)
9. 题库 [https://leetcode-cn.com/problemset/concurrency/](https://leetcode-cn.com/problemset/concurrency/)

vue的element使用，遇到的问题



A。 返回顶部组件，很简单的组件，坑在target这里，.main-box是我项目里面外层父元素的class名，.el-scrollbar__wrap，是官方自带的。
   【 target表示目标dom, 这里即为el-main盒子的类名 】
   【 el-backtop里面包裹的内容可以自定义换成需要的样式 】
   【 因为原本项目中已经使用了el-scrollbar，element的隐藏组件，可能是影响到了，最开始这个组件怎么也展示不出来。】
    其他问题出现，如何解决， https://juejin.cn/post/6844904181954773006
    
<el-backtop target=".main-box .el-scrollbar__wrap">
    <div>
      <i class="el-icon-top"></i>
    </div>
  </el-backtop>
  
  .el-backtop {
     right: 40px !important;
     bottom: 100px !important;
     width: 62px;
     height: 62px;
     background: rgba(0, 0, 0, 0.15);
     border-radius: 50%;
     display: flex;
     justify-content: center;
     align-items: center;
     box-shadow: 0 0 0px white !important;
     z-index: 999;
     i {
       font-size: 30px;
       color: #ffffff;
     }
     &:hover {
       background: rgba(0, 0, 0, 0.35);
     }
  }

。。。。。。。。。。。。。。。。。。。。。。。。。。

B。 分页的展示，element-ui 分页中的slot的用法\(自定义分页显示内容\) 

官网![截屏2021-08-25下午2 55 44](https://user-images.githubusercontent.com/49188120/130747951-8e6efe20-4bfe-4861-9f4f-843a2e425f85.png)

我们想要：![&#x622A;&#x5C4F;2021-08-25&#x4E0B;&#x5348;2 54 26](https://user-images.githubusercontent.com/49188120/130743616-c4de42e0-78b8-4dee-9dd8-72d6587acef9.png) 

所以需要我们调整一下分页

![&#x622A;&#x5C4F;2021-08-25&#x4E0B;&#x5348;3 27 21](https://user-images.githubusercontent.com/49188120/130745843-b7f139b0-4d47-46f2-bbe4-c0bcd5d1426a.png) 
![&#x622A;&#x5C4F;2021-08-25&#x4E0B;&#x5348;3 27 26](https://user-images.githubusercontent.com/49188120/130745847-159aacd6-beaa-4e3a-92c9-6c44c2fa4c8f.png)  
【 layout 里面的值可以随意改变位置，以达到我们所需要的效果。】
<el-pagination
   background
   layout="prev, pager, next, slot, jumper"
   prev-text="上一页"
   next-text="下一页"
   :current-page="form.page_id"
   :total="pageTotal"
   @current-change="onPageChange"
 >
   <span class="goodsFont">共 {{ totalShow }} 页</span>
 </el-pagination>

