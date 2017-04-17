## url输入到页面展现的过程

- ### 地址栏中输入网址
我们一般输入的网址如："www.baidu.com"称为域名，目的是为了方便记忆。但计算机只识别IP；所以就需要有一个IP和你所输入的域名相对应，以便计算机识别，这就需要域名解析。

- ### 域名解析
域名解析通俗的讲就是查找你输入的网址所对应的IP地址；通常会按以下条件依次查找：

1. 通过浏览器缓存：之前浏览过的网址会被记录下来，所以当再次进入时首先从这个查找有没有记录，有的话直接用就ok。

2. host文件中的系统缓存：（**被谁记录下的？**）host文件会有一些域名的IP地址的记录，当浏览器缓存没有查找到的话，会在这里进行再次查找。

3. 路由器缓存：路由器也会有一些记录，当前两次未查找到，会在这里找找看。

4. ISP运营商DNS缓存：ISP是互联网服务提供商，如：电信，联通...，他们的服务器中有大量的域名-IP记录；首次登陆一个网站也应该是从他们那里拿到网站对应的ip。

> 有时我们上不了网了，有人会建议你修改DNS里的值，如8.8.8.8 /114.114.114.114  就是换个地方找；电信的找不到，我换阿里的试试。

> DNS劫持，原理就是把网址所对应的正确的IP换成一个错的。


5. 如果连运营商那里都没有怎么办？会向根域名查找，一层一层查看，直到找到位置，但前提是你输入的网址是真的。

- ### 向服务器发送请求


- ### web服务器接受、处理请求
通过上面的跋山涉水终于找到了域名对应的ip，到这里可以向web发送请求给我资源了；
其中的处理过程简化为**MVC**（以后再写）；之后web服务器网页所呈现的资源发送到浏览器当中

- ### 服务器发回数据到页面（html、css、js、image...）
服务器送来了一堆东西（html、css、js、image...），浏览器通过解析、渲染...最终在页面上呈现出一张页面。
