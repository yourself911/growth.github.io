# ydty说明书    

### 打开知晓云控制台,可以在左侧栏看 开发 这块区域。   

* 数据
    - 数据表存放位置
* 文件
    - 在此上传文件，可拷贝链接到数据表字段中    
    
* 用户
    - 查看用户的详细信息
* 支付
    - 查看用户的支付信息，可进行退款操作
    

### 涉及的数据表   

<img src="{{site.url}}/images/table.png" />

> 其中user表没什么用处了，用_userprofile代替了。    

### 操作数据表

> 鼠标悬浮在course (meta) 可以查看该表的描述。    

> <img src="{{site.url}}/images/see-table.png" align="left"/>

> 鼠标悬浮在 字段上 可以查看该字段的描述。   

> <img src="{{site.url}}/images/see-field.png" align="left" />

​    

> 鼠标悬浮在 ··· 图标可进行如下操作。

> <img src="{{site.url}}/images/operation.png" align="left" />

> 点击每行最右边的 编辑 进行修改行数据 。

> <img src="{{site.url}}/images/edit.png" align='left'/>

> 点击添加行 新增数据  
>
> <img src="{{site.url}}/images/row.png" align="left" />
>
> 

> _userprofile 表  ： 用户信息存放处

| 字段      | 描述                                                         |
| :-------- | :----------------------------------------------------------- |
| integral  | 用户积分数                                                   |
| _username | 资料设置里的用户名                                           |
| realname  | 资料设置里的孩子姓名                                         |
| phone     | 资料设置里的手机号码                                         |
| age       | 资料设置里的孩子年龄                                         |
| address   | 资料设置里的地址                                             |
| sex       | 资料设置里的性别                                             |
| position  | 个人中心的用户称号，这个由运营人员设置，默认值为学员         |
| coach     | 教练id, 对应的position也为某某教练，这个值为coach表中的id,粘贴复制即可 |

> coach 表： 教练信息     这个什么要说的



> course 表: 课程信息  

| 字段         | 描述                                                         |
| ------------ | ------------------------------------------------------------ |
| name         | 课程名称                                                     |
| price        | 课程价格                                                     |
| des          | 课程详情里的课程介绍，这是个富文本，**请使用富文本编辑器，图文并茂** |
| courseTime   | 课程详情里的上课时间，这是一个字符串                         |
| total        | 课程总课时数                                                 |
| content      | 课程内容 暂时没用                                            |
| coverPic     | 课程封面，注意：不是课程详情里的图片                         |
| students     | 暂时没用                                                     |
| is_saling    | 暂时没用，直接删除课程就算下架了                             |
| frequency    | 暂时没用                                                     |
| intro        | 课程简介，课程名称下方的内容，课程详情价格下的内容           |
| store        | 课程所属门店，值为store表中，记录中的id，目前只有一个门店，所以值都一样，手动复制粘贴 |
| times        | 课程每个课时所对应的时间，**注意：这个很重要，一定要填写好，下面会给出操作**。 |
| imgs         | 课程详情里的图片，点击可预览                                 |
| coach        | 课程对应的教练id，一定得有                                   |
| busLocation  | bus等待地点名称，**注意: 默认值为0，如果没有地点，请不要修改这个默认值，我是根据这个值进行判断要不要显示等待地点的。** |
| busLatitude  | 纬度（https://maplocation.sjfkai.com/ 该网站查询）然后复制粘贴就行了 |
| busLongitude | 经度                                                         |

> 添加 修改 课程课时时间
>
> 点击编辑，弹出修改数据行框，
>
> 在times 字段中，点击右边的加减号 进行添加删除。点击框内小小的日历图标进行日期时间的选择
>
> imgs字段中的图片url，直接到开发-->文件 中复制已上传的文件链接

<img src="{{site.url}}/images/times.png" align="left" />



> consult 表： 首页的培训咨询信息， 这个看知晓云就行了，
>
> 鼠标悬浮在右边的 ··· 图标上，点击导出，选择导出的选项，即可导出数据。

<img src="{{site.url}}/images/export.png" align="left" />



> discover 表: 发现 --> 视频页面的数据

| 字段     | 描述                                                         |
| -------- | ------------------------------------------------------------ |
| coverPic | 封面图片地址                                                 |
| url      | 视频地址，点击选择文件，弹出一个选择文件框，选择你在文件中上传的MP4资源 |
| des      | 描述                                                         |
| type     | 没用                                                         |



> banner 表: 首页轮播图，这个看知晓云数据表就知道的了



> investment 表： 发现--> 加盟异动 里输入的数据, 只需查看即可



> recruit 表: 发现--> 招聘里输入的信息， 查看即可  



> store 表： 门店信息

| 字段      | 描述                                                     |
| --------- | -------------------------------------------------------- |
| name      | 店名                                                     |
| price     | 暂时没用                                                 |
| des       | 暂时没用                                                 |
| coverPic  | 门店封面                                                 |
| location  | 门店地址                                                 |
| phone     | 暂时没用                                                 |
| latitude  | 纬度(https://maplocation.sjfkai.com/ 该网站查询)         |
| longitude | 经度                                                     |
| attention | 门店详情的注意事项，**注意：这是一个字符串，不是富文本** |
| imgs      | 门店详情的图片                                           |
| step      | 门店详情的健身步骤的图片                                 |



> concat 表： 只存储一个联系客服的电话号码



>  goododer 表： 用户购买积分商城的订单表 ， 没什么可说的



> goods 表： 积分商品表 

| 字段      | 描述                                                         |
| --------- | ------------------------------------------------------------ |
| title     | 商品名称                                                     |
| price     | 商品价格                                                     |
| logo      | 商品封面                                                     |
| inventory | 商品数量                                                     |
| imgs      | 商品详情内的多张图片                                         |
| detail    | 商品的详情，**注意： 这是一个富文本，请使用富文本编辑器，图文并茂** |



> order 表： 课程订单信息记录

| 字段                    | 描述                                           |
| ----------------------- | ---------------------------------------------- |
| status                  | 支付状态： 支付成功，支付失败                  |
| total_cost              | 支付金额                                       |
| create_time 和 pay_time | 直接看create_at    update_at                   |
| course                  | 购买的课程id                                   |
| name                    | 购买时填写的姓名                               |
| phone                   | 购买时填写的电话号码                           |
| wechat                  | 购买时填写的微信号                             |
| address                 | 购买时填写的地址                               |
| coachId                 | 购买时填写的教练id                             |
| user                    | 该买的用户id，关联_userprofile表，点击即可跳转 |
| inclass                 | 用户的上课记录id,关联 inclass 表               |



> inclass 表： 用户上课记录数据   对应的小程序页面是 进入课程 页面
>
> 这一块的处理是：当天有课才能进行请假或签到，两者只能取一，互斥关系

| 字段         | 描述                                                         |
| ------------ | ------------------------------------------------------------ |
| studyCount   | 学员已经学习的课程数                                         |
| coach_remark | 教练评语，由运营人员进行操作，**这不是富文本,注意确认好 学员 进行评价哈** |
| memoir       | 教练对学员的 课程 实录 也就是一些 上课图片 **,注意确认好 学员 进行评价哈** |
| signIn       | 学员上课的签到记录，                                         |
| leave        | 学员请假记录                                                 |



> 后续会增加一些 字段，一个积分计算表，使用直接知晓云数据表描述



###  文件

> 上传
>
> <img src="{{site.url}}/images/upload.png" />



### 支付

> 退款
>
> <img src="{{site.url}}/images/refund.png" />


<img src="{{site.url}}/images/canvas-shadow.png" style="width: 160px; height: 160px;" />
