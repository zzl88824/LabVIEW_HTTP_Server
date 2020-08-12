# LabVIEW_HTTP_Server
An HTTP server implemented using LabVIEW basic functions.
<br>
在使用LabVIEW进行网络编程的时候，遇到两个问题：<br>
    1. 在Linux(x86)版本下无法创建Web Service；<br>
    2. 使用LabVIEW NXG版本开发的web应用程序，部署在NI Application Server(8080端口)上，由于个别文件过大(例如\ni-webvi-resource-v0\DeployedRun.min.js，3.34MB)造成加载速度缓慢。<br>
为了解决以上问题，使用LabVIEW编写了一个HTTP服务器，实现了基于基础的TCP/IP函数的Web Service服务程序，该程序同时实现了发送静态文件的功能。<br>
使用GZIP对DeployedRun.min.js文件进行的压缩，并且返回压缩后的内容，提高了页面文件的加载速度。<br>
