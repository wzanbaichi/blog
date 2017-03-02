#第一步. 在浏览器输入URL
##URL是什么
-URL: 统一资源定位符，用于定位互联网上的资源
-http、https、ftp、file 协议
#第二步. 域名解析
对于 http://jirengu.com 的URL，浏览器实际上不知道 jirengu.com到底是什么东西，需要查找jirengu.com网站所在服务器的IP地址，才能找到目标
##域名是什么
对于http://jirengu.com:8080/blog , jirengu.com就是域名
##IP地址是什么
-每个处于互联网中的设备都有IP 地址，形如 192.168.0.1
-局域网 IP 和公网 IP 是有差别的
-127.0.0.1代表本机的 IP
##域名解析的流程
1. 浏览器缓存 – 浏览器会缓存DNS记录一段时间
2. 系统缓存 - 从 Hosts 文件查找是否有该域名和对应 IP。
3. 路由器缓存 – 一般路由器也会缓存域名信息。
4. ISP DNS 缓存 – 比如到电信的 DNS 上查找缓存。
5. 如果都没有找到，则向根域名服务器查找域名对应 IP，根域名服务器把请求转发到下一级，知道找到 IP
                        1. 电脑上不了网，为什么修改dns为8.8.8.8 或者114.114.114.114?
			                        2. dns 劫持是什么？
						#第三步. 服务器处理
						服务器是一台安装系统的机器，常见的系统如Linux、windows server 2012系统里安装的处理请求的应用叫 Web server
						##Web服务器
						-常见的 web服务器有 Apache、Nginx、IIS、Lighttpd
						-web服务器接收用户的Request 交给网站代码，或者接受请求反向代理到其他 web服务器
						![](http://upload-images.jianshu.io/upload_images/4988561-56632543028fa2ef.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
						#第四步. 网站处理流程
						![MVC 模型(model)-视图(view)-控制器(controller)](http://upload-images.jianshu.io/upload_images/4988561-cffd29fccf6ba074.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
						#浏览器处理

						HTML字符串被浏览器接受后被一句句读取解析

						解析到link 标签后重新发送请求获取css

						解析到 script标签后发送请求获取 js，并执行代码

						解析到img 标签后发送请求获取图片资源
						#绘制网页
						浏览器根据 HTML 和 CSS 计算得到渲染树，绘制到屏幕上

						js 会被执行
