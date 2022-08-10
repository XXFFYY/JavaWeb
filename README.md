# JavaWeb
JavaWeb学习

---

## 1.HTML中的基础标签

​	**HTML是解释型的文本标记语言，不区分大小写**

---



### 1.1  html标签

```html
<!--html页面中由一对标签组成：<html></html>
  <html>称之为 开始标签
    </html>称之为 结束标签-->
    <html>
        ...
</html>
```

---

### 1.2 标题标签

```html
<!--title表示网页的标题-->
<head>
    <title>这是我的第一个网页</title>
  </head>
```

---

### 1.3 编码标签

```html
<!--可以在mate标签中设置编码方式-->
<head>
  <title>这是我的第一个网页</title>
  <meta charset="UTF-8">
</head>
```

---

### 1.4 换行标签

```html
<!--<br/>表示换行。br标签是一个单标签-->
<br/>
```

---

### 1.5 段落标签

```html
<!--p表示段落标签-->
<p>这是一个段落</p>
<p>这是第二个段落</p>
```

---

### 1.6图片标签

```html
<!--img表示图片标签
        src表示图片的路径
        width表示图片的宽度
        height表示图片的高度
        alt表示图片的描述-->
 <img src="/WEB-INF/templates/imgs/demo.jpg" width="57" height="73" alt="这是一张图片"/>
```

---

### 1.7 标题标签

```html
<!--h1~h6：标题标签-->
	<h1>标题一</h1>
    <h2>标题一</h2>
    <h3>标题一</h3>
    <h4>标题一</h4>
    <h5>标题一</h5>
    <h6>标题一</h6>
```

---

### 1.8 列表标签

```html
<!--列表标签:
      ol:有序列表
        start表示从*开始，type显示的类型：A a I i 1(default)
      ul:无序列表
        type:disc(default) circle square-->
武林高手排行榜:
    <ol type="i" start="3">
      <li>扫地僧</li>
      <li>萧远山</li>
      <li>慕容博</li>
      <li>虚竹</li>
      <li>阿紫</li>
    </ol>
    武林大会人员名单：
    <ul type="circle">
      <li>乔峰</li>
      <li>阿朱</li>
      <li>马夫人</li>
      <li>白世镜</li>
    </ul>
```

---

### 1.9 下划线、加粗、斜体标签

```html
<!--u下划线 b加粗 i斜体-->
你是喜欢<b>甜</b>月饼还是<i>咸</i><u>月饼</u>？
```

---

### 1.10上标、下标标签

```html
<!--上标：sup 下标：sub-->
水分子的化学式：H<sub>2</sub>O<br/>
10的平方等于100：10<sup>2</sup>=100<br/>
```

---

### 1.11HTML中的实体

```html
<!--HTML中的实体：小于号：&lt; 小于号：&gt; 双引号：&quot; 单引号：&apos;-->
	5小于10:5&lt;10<br/>
    10大于5:10&gt;5<br/>
    5小于等于10:5&le;10<br/>
    10大于等于5:10&ge;5<br/>
    注册商标 &reg;<br/>
    版权符号 &copy;
```

---

### 1.12不换行的块标记

```html
<!--span 不换行的块标记-->
<span>赵又廷</span>，夺妻之仇
```

---

### 1.13超链接标签

```html
<!--a表示超链接
      href表示超链接的地址
      target:
        _self:当前窗口打开
        _blank:新窗口打开
        _parent:父窗口打开
        _top:在顶层窗口打开-->
<a href="https://www.baidu.com" target="_blank">百度一下</a>
```

---

### 1.14表格标签

```html
<!--表格 table
    行:tr
    列:td
    表头列:th
    table中有如下属性（虽然已经淘汰，了解）
    -border:表格边框的宽度
    -width：表格宽度
    -cellspacing：表格中的单元格之间的间距
    -cellpadding：表格中的单元格之间的内边距

    tr中有一个属性：align，表示行的对齐方式，可以是left,center,right

    rowspan：行合并
    colspan：列合并-->
<table width="600px"  border="1" cellpadding="4" cellspacing="0">
      <tr align="center">
        <th>名称</th>
        <th>单价</th>
        <th>数量</th>
        <th>小计</th>
        <th>操作</th>
      </tr>
      <tr align="center">
        <td>苹果</td>
        <td rowspan="2">5</td>
        <td>20</td>
        <td>100</td>
        <td><img src="imgs/del.jpg" width="24"></td>
      </tr>
      <tr align="center">
        <td>菠萝</td>
        <!--<td>5</td>-->
        <td>15</td>
        <td>45</td>
        <td><img src="imgs/del.jpg" width="24"></td>
      </tr>
      <tr align="center">
        <td>西瓜</td>
        <td>6</td>
        <td>6</td>
        <td>36</td>
        <td ><img src="imgs/del.jpg" width="24"></td>
      </tr>
      <tr align="center">
        <td>总计</td>
        <td colspan="4">181</td>
      </tr>
    </table>
```

---

### 1.15 表单标签

```html
<!--表单 form
      input type="text"表示文本框，其中name属性必须要指定，否则这个文本框的数据将来是不会发送给服务器的
      input type="password"表示密码框
      input type="radio"表示单选按钮。需要注意的是，name属性值保持一致，这样才有互斥效果；可以通过checked属性设置默认选项
      input type="checkbox"表示复选框。name属性值建议保持一致，这样将来我们服务器端获取的值是一个数组
      select表示下拉框，每一个选项是option，其中value属性是发给服务器的值，selected表示默认
      textarea 表示多行文本框（或称之为文本域），它的value值就是开始结束标签之间的内容
      input type="submit"表示提交按钮
      input type="reset"表示重置按钮
      input type="button"表示普通按钮-->
<form action = “demo05.html” method="post">
      昵称:<input type="text" name="nickName" value="请输入你的昵称"/><br/>
      密码:<input type="password" name="pwd"/><br/>
      性别:<input type="radio" name="gender" value="male" checked/>男
          <input type="radio" name="gender" value="female"/>女<br/>
      爱好:<input type="checkbox" name="hobby" value="basketball" checked/>篮球
          <input type="checkbox" name="hobby" value="football"/>足球
          <input type="checkbox" name="hobby" value="earth"/>地球<br/>
      星座:<select name="star" >
              <option value="1">白羊座</option>
              <option value="2">金牛座</option>
              <option value="3" selected>双鱼座</option>
              <option value="4">射手座</option>
              <option value="5">双子座</option>
              <option value="6">天秤座</option>
          </select><br/>
      备注:<textarea name="remark" rows="4" cols="50"></textarea><br/>
      <input type="submit" value="注 册">
      <input type="reset" value="重置">
      <input type="button" value="普通按钮">
    </form>
```

---



