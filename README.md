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

返回顶部组件，

【 分页的展示，element-ui 分页中的slot的用法(自定义分页显示内容)
    官网 ![截屏2021-08-25下午2 55 44](https://user-images.githubusercontent.com/49188120/130743279-247ccc6f-2432-484a-910e-27980f150d5a.png)
    我们想要：![截屏2021-08-25下午2 54 26](https://user-images.githubusercontent.com/49188120/130743616-c4de42e0-78b8-4dee-9dd8-72d6587acef9.png)
    所以需要我们调整一下分页
    ![截屏2021-08-25下午3 27 21](https://user-images.githubusercontent.com/49188120/130745843-b7f139b0-4d47-46f2-bbe4-c0bcd5d1426a.png)
    ![截屏2021-08-25下午3 27 26](https://user-images.githubusercontent.com/49188120/130745847-159aacd6-beaa-4e3a-92c9-6c44c2fa4c8f.png)
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
          </el-pagination> 】
          
         



































