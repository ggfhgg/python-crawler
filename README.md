# python-crawler

www.virus.total这个网站采用了shadow-dom形式，将元素信息隐藏在子节点当中
并进行了反爬虫处理（爬的太快或短时间内发送大量请求都会被拒绝访问）
并且所有的数据是通过一个API接口以压缩包的形式动态加载的。
所以我采用了selenium库用来模拟浏览器的行为动态加载；
并对shadow-root根节点进行深度拆解，以强制休眠方式绕开次数限制，最终爬取到md5值和文件名称等信息。

NOTICE：
  使用selenium前需要根据自己的浏览器类型和版本，选择对应的浏览器驱动，比如我下载的是Chromedriver.exe，并且需要把驱动复制到浏览器安装目录里
  （C:\Program Files (x86)\Google\Chrome\Application）
