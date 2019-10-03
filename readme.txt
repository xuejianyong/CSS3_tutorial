CSS3 选择器

1. 通过标签名获取html对象
        <style type="text/css">
            p { ... } <!-- 选择所有 p 标签 -->
            div p { ... } <!-- 范围限定 | 选择 div 里面的 p 标签  -->
        </style>

        <p> p1 ~ </p>
        <div>
            <p> p2 ~ </p>
            <p> p3 ~ </p>
        </div>


2. 通过class属性获取html对象
        <style type="text/css">
        .jmjc { .. } <!-- 选择所有 class="jmjc" 的元素 -->
        div .jmjc { ... } <!-- 范围限定 -->
        </style>

        <p class="jmjc"> p1~ </p>
        <div>
            <p class="jmjc"> p2~ </p>
            <p class="jmjc"> p3~ </p>
        </div>


3. 通过id属性获取html对象
        <style type="text/css"> 
            #jmjc { ... } <!-- 选择 id="jmjc" 的元素 -->
        </style>

        <p id="jmjc"> p1 ~ </p>
        <p id="jmjc"> 错误 </p> <!-- 不同于 class 的性质，id 是唯一的，值不可以重复  -->


4. 通过属性值获取html对象
        <style type="text/css"> 
            [type="text"] { ... }
            input[type="text"] { ... } <!-- 同上 -->
        </style>

        <input type="text"> <!-- 被选中 -->
        <input type="password">


5. 通过 ， 合并不同的选择器
        <style type="text/css"> 
            p, div { ... }  <!-- 如果 p & div 设置的样式相同，可以合并在一起设置 -->
        </style>

        <p> p ~ <p>
        <div> div ~ </div>


6. 子类选择器
        <style type="text/css"> 
            div strong { ... } <!-- 所有级选择 | 两个 strong 都被选择 -->
            div > strong { ... } <!-- 二级选择 | 只能选择到 strong 1 ～ -->
        </style>

        <div>
        <strong> 1 ~ </strong>
        <p><strong> 2 ~ </strong></p>
        </div>


7. 子类过滤器
        <style type="text/css"> 
            p:first-child { ... } <!-- 选择第一个 p -->
            p:nth-child(2) { ... } <!-- 指定选择第几个 p -->
            p:last-child { ... } <!-- 选择最后一个 p -->
        </style>

        <p> p1 ~ </p>
        <p> p2 ~ </p>
        <p> p3 ~ </p>


8. 星号选择器
        一般网页的默认字体大小是 14px、默认的背景颜色是 白色、默认的链接有 下划线，这些值我们称为初始化样式。
        * { ... } <!-- * 号选择器可以重新声明初始化样式 -->

