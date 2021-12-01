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

1.httpbin.org网站的车市URL为：https://httpbin.org/status/{codes}

+ https://httpbin.org/status/100 无法获取

+ https://httpbin.org/status/200 请求成功

  Success（成功状态码）--请求正常处理完毕

  2.response结果与get