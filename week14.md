时间:2021-12-01

1.httpbin

2.httpbin 下载

3.curl安装

###  2.Auth methods

1，通过URL路径中提交验证信息[

/basic-auth/{user}/{passwd}]

prompts the user for authorization using HTTP Basic Auth.

2.例如

> 1.user=lihua
>
> 2.passwd=123456
>
> 3.通用：URL=https://httpbin.org/basic-auth/{user}{passwd}
>
> 4.本案例：UPL=https://httpbin.org/basic-auth/lihua/123456

3.通过访问想要验证的URL地址，填入正确的注册信息（user的和passwd)

+ 200:

+ ```json
  {
    "authenticated": true,
    "user": "lihua"
  }
  ```

  

### status codes

1. httpbin.org网站的测试URL为 ：http://httpbin.org/status/{codes}

   > - 注意： 在用该网站测试状态码时，没有对应的body信息（页面信息）

2. 状态码测试结果：

   > 1. http://httpbin.org/status/100
   >
   > > 1. Informational（信息性状态码）- 接收的请求正在处理 ----加载中...
   > > 2. 类型错误：无法获取
   >
   > 1. http://httpbin.org/status/200
   >
   > > 1. *Success*（成功状态码）--请求正常处理完毕
   > > 2. response结果 与 get (https://httpbin.org/get)测试相同(但不包含页面信息)
   >
   > 1. http://httpbin.org/status/300
   >
   > > 1. Redirection（重定向状态码） --- 需要进行附加操作以完成请求
   > >
   > > 2. ```
   > >    Status Code: 300 MULTIPLE CHOICES (from disk cache)
   > >    ```
   >
   > 1. http://httpbin.org/status/400
   >
   > > 1. Client Error（客户端错误状态码） -- 服务器无法处理请求
   > > 2. 无响应内容，请客户检查请求信息（URL）是否正确，或者请求方式（如GET、POST）是否正确
   >
   > 1. http://httpbin.org/status/500
   >
   > > 1. Server Error（服务器错误状态码）--服务器处理请求出错
   > > 2. 服务端报错的处理方法，找到服务人员（如客服等）询问网站问题，服务端人员通过检查后端代码解决。

   # 4. 请求检查

   1. 检查首部信息

   > 1. 测试的URL路径： http://httpbin.org/headers
   > 2. 返回页面信息是请求客户端的**请求者**首部信息，结果如下：
   >
   > ```
   > {
   >   "headers": {
   >     "Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3", 
   >     "Accept-Encoding": "gzip, deflate", 
   >     "Accept-Language": "zh-CN,zh;q=0.9", 
   >     "Host": "httpbin.org", 
   >     "Upgrade-Insecure-Requests": "1", 
   >     "User-Agent": "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/77.0.3865.120 Safari/537.36", 
   >     "X-Amzn-Trace-Id": "Root=1-61a75fd2-2ac5bca342c771fc158960c5"
   >   }
   > }
   > ```

   1. 检查**请求者**的ip地址：

   > 1. 测试的URL路径： http://httpbin.org/ip
   > 2. 返回结果为：
   >
   > ```
   > {
   >   "origin": "210.21.79.244"
   > }
   > ```

   1. 检查请求者的网络代理

   > 1. 测试的URL路径： http://httpbin.org/user-agent
   > 2. 返回结果为:
   >
   > ```
   > {
   >   "user-agent": "Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/77.0.3865.120 Safari/537.36"
   > }
   > ```

# 5. 图片信息

1. 测试链接：http://httpbin.org/image

2. 返回信息： 一张测试图片

   ![img](http://httpbin.org/image)

# 6. 课后请先查阅： [Face⁺⁺ - 旷视Face⁺⁺人工智能开放平台](https://www.faceplusplus.com.cn/)