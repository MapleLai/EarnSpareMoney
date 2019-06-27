# readme

URL前缀：http://happyzhier.club:3000

- 登录

  **PUT**:`/login`

  request body = {"uid" : [用户名], 

  ​				"passwd" : [密码]}

- 注册

  **POST**：`/register`

  request body = {"uid" : [用户名], 

  ​				"passwd" : [密码],

  ​				"nickname":[昵称],

  ​				"signature":[个性签名],

  ​				"img_url":[头像],

  ​				"tel":[电话],

  ​				"school":[学校],

  ​				"money":[金额],

  ​				"credit":[信用度]}

  >登录/注册会返回一个JSON数据，查看“msg”就可以知道提交结果，提交成功的话“msg”字段是“success”，错误的情况会有相应的提示信息。
  >
  >

- 获取个人信息

  **GET**:`/user?uid=[用户名]`

- 修改个人信息

  **PUT**:`/user`

  request body = {"uid" : [用户名], 

  ​				"passwd" : [密码],

  ​				"nickname":[昵称],

  ​				"signature":[个性签名],

  ​				"img_url":[头像],

  ​				"tel":[电话],

  ​				"school":[学校],

  ​				"money":[金额],

  ​				"credit":[信用度]}

- 获取单个任务信息

  **GET**:`/mission?mid=[任务序号]`

- 获取所有任务信息

  **GET**:`/missions`

- 提交任务

  **POST**:`/misson`

  request body = { "title" : [标题],

  ​				"uid":[发布人],

  ​				"reward":[报酬],

  ​				"mtype":[任务类型],

  ​				"description": [任务描述],

  ​				"imgs_url": [图片],

  ​				"people_limit":[期望参与人数],

  ​				"people":[已参与人数],

  ​				"ing":[任务是否进行中]}

- 参加任务

  **POST:**`participate`

  request body = { "mid" : [任务序号],

  ​				"uid":[参与人]}

- 完成任务

  **PUT:**`finish`

  request body = { "mid" : [任务序号],

  ​				"uid":[参与人]}

- 删除任务

  **DELETE:**`mission`

  request body = { "mid" : [任务序号]}

- 取消参与任务

  **DELETE:**`participate`

  request body = { "mid" : [任务序号],

  ​				"uid":[参与人]}