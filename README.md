# 基于线程池的简单Web服务器项目

**应用技术：Linux、Epoll、Socket、 TCP**  
**项目描述：**   
  此项目是基于轻量级线程池的多线程Web服务器，使用Epoll进行多路复用。应用层使用有限状态机对HTTP请求进行解析，支持静态资源的访问和通用网关(CGI)的动态消息回显。  
**主要工作：**  
- 采用Reactor模式，使用Epoll进行事件的监听；
- 创建固定的线程池，使用信号量将HTTP请求处理分解为生产者-消费者模型；
- 使用内存映射，实现GET的静态文件请求;
- 采用CGI脚本对POST动态请求进行回显，使用管道进行服务器与CGI程序间的通信。
