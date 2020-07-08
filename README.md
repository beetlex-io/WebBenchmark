# WebBenchmark
`WebBenchmark`是一款基于开源通讯组件`Beetlex`扩展的`Webapi`管理和性能测试工具，在传统工具中一般管理工具缺乏性能压测能力或有性能测试的缺少管理功能；`WebBenchmark`的设计目标是就管理和性能压测能力同时具备。
## 演示地址
http://webbenchmark.beetlex.io/
## 功能
- 支持HTTP和HTTPS的服务测试
- 暂只支持基础方法的GET,POST,PUT和DELETE
- 支持多用户和多分类管理
- 提供访问API详细时间线信息
- 提供值函数支持，可以更好地进行随机性数据构建和压测
- 支持多用例同时压测
- 提供详细的响应状态和各延时汇总
## 计划加入的功能
- 支持文件上传功能
- 支持多节点测试

## v0.8.7
- 修复性能测试状态存在异常的错误
- 添加基础用例导出和导入功能
- 性能测试保存历史记录并可以查看历史结果
- 性能测试状态显示增加明细各种状态码的情况

## 安装
工具是基于`.netcore`开发，可以运行在安装有.net core 2.1或更高版本的各大平台上。下载最新版本的压缩包，根据不同平台运行`run.sh`或`run.bat`.工具默认占用80端口，如果存在端口被占用问题可以编辑以上两个文件修改对应启动端口。
启动后可以通过浏览器访问相关服务，初始的用户名和密码是:`admin`和`123456`.进入服务后工具界面如下：


![image](https://user-images.githubusercontent.com/2564178/86763474-f0197f00-c079-11ea-88ff-38a85ff279a4.png)


![image](https://user-images.githubusercontent.com/2564178/86763543-fc054100-c079-11ea-9e31-9e441d47678a.png)

## 新建用例
工具的首页面是基础用例管理，在这里可以添加、管理和测试webapi的用例 ;通过点击添加按钮可以新增一下基础的测试用例 

![image](https://user-images.githubusercontent.com/2564178/86766720-826f5200-c07d-11ea-8c26-127fe6758bee.png)

添加的信息主要包括有基础用例信息和相关HTTP请求内容描述。
- **地址参数**
 
  主要是包括在Url里面的参数，参数可以根据自己的需要来添加并设置.
![image](https://user-images.githubusercontent.com/2564178/86766744-8d29e700-c07d-11ea-912a-8788200128fd.png)
参数值支持函数引用，通过函数即可以在每次请求的都产生新的函数值进行提交。

- **请求头**

  主要可以添加一些请求头信息，如token和User-agent等。
![image](https://user-images.githubusercontent.com/2564178/86766770-961ab880-c07d-11ea-8c59-189ac3c11358.png)
  
- **请求内容**

  工具暂只支持`application/json`和`form-urlencoded`两种，工具还专门为json提供更简便和具备验证能力的编辑器方便录入
![image](https://user-images.githubusercontent.com/2564178/86766796-9fa42080-c07d-11ea-9bbe-459599c7edb2.png)

- **测试**

  组件在编辑的时候就对当前用例进行一个测试，通过测试可以了解到当前用例运行的实际情况(包括整个测试过程的一些网络请求响应时间线).
![image](https://user-images.githubusercontent.com/2564178/86766835-aaf74c00-c07d-11ea-8b1b-165bc9b5f3d7.png)


## 批量测试
工具支持单个或批量测试用例,只要选择相关用例进行批量测试即可

![image](https://user-images.githubusercontent.com/2564178/86766860-b34f8700-c07d-11ea-9c8d-fd92ef3a8f71.png)

批量测试完成后即可实时查看每个用例的测试情况和相关处理时间线。

## 性能测试
工具提供多用例组合性能测试，只需要在创建性能测试用例时选择需要压测的用例即可。

![image](https://user-images.githubusercontent.com/2564178/86766885-bc405880-c07d-11ea-8659-51c16107b1fb.png)
保存好相关性能测试用例即保存到相关列表中

![image](https://user-images.githubusercontent.com/2564178/86766918-c5312a00-c07d-11ea-8662-accec294370a.png)


这时候就可以点击相关用例测试按钮进入到性能测试页面

![image](https://user-images.githubusercontent.com/2564178/86766937-cbbfa180-c07d-11ea-9c44-365429378650.png)

这时候可以根据自己需求设置相关并发测试的数据进行一个压力测试。

![image](https://user-images.githubusercontent.com/2564178/86766957-d4b07300-c07d-11ea-967f-1a0d920fd04f.png)

工具在测试过程中实时反映当前压测的结果，并把相关状态和相应延时分布数据详细显示出来。如果想查看压测过程中某个请求的详细情况，可以点击相关用例 即可显示该用户的详细情况

![image](https://user-images.githubusercontent.com/2564178/86766977-dc701780-c07d-11ea-9688-51e0a8010426.png)



以上是工具使用的相关介绍，有些功能在免费版本中受限。想更多了解可以查看在线演示 http://webbenchmark.beetlex.io/

