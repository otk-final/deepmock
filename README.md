# deepmock
一个在线模拟http响应工具

<a href="http://console.deepmock.cn" target="_blank"> 在线使用</a> | [控制台]

### 谁在用？

1. 前端开发人员需要模拟真实网络数据时，后端开发快速定义接口格式和mock数据进行联调测试
2. 模拟真实网络环境（延迟）
3. 模拟服务器繁忙（并发，限流，队列）

##### 架构图

![image](https://github.com/otk-final/deepmock/blob/main/image/flow.png)

#### 特性

##### 模拟场景（可多选）

- [x] 认证（Basic)
- [x] 队列
- [x] 并发
- [x] 延迟
- [x] 限流

##### 路由

对同一接口，不同请求参数（`path` ，`header`，`query`）设置不同响应模式

##### 响应模式（单选）

1. 转发
   1. 支持重写响应头
2. 模拟
   1. 支持自定义响应码
   2. 支持自定义响应头
   3. 支持自定义响应体
   
##### 支持响应类型

1. 普通文本格式    `json` ，`xml`， `html`， `text`

   自定义

2. sse服务端推送    `text`

   自定义内容（换行），默认响应头`content-type`：`text/event-stream`， 每`1秒`输出一行文本，

#### http

![image](https://github.com/otk-final/deepmock/blob/main/image/http.png)

#### websocket

自定义websocket端点，用于真实客户端接入，通过console控制台发送消息和真实客户端进行通信联调

![image](https://github.com/otk-final/deepmock/blob/main/image/ws.png)

#### 快捷测试（简易版Postman）

受限于浏览器安全策略，不允许在线调试`https`接口

![image](https://github.com/otk-final/deepmock/blob/main/image/test2.png)

#### 承诺

1. 无需登陆。
2. 不保留任何请求数据和转发数据。
3. 根据`浏览器指纹ID`生成独立`二级域名`进行数据隔离。
4. 工具仅适合开发环境联调测试，请勿生产环境使用！！！

