# SZhe_Scan
碎遮 Web漏洞扫描器

自动化扫描特定范围web资产，python多线程搜集目标信息，获取页面url链接，对常见高危漏洞进行扫描检测，并可以自己添加POC进行漏洞检测，最后将结果可视化显示在界面上

环境要求:

    python版本要求：3.x，python运行需要的类库在requirements.txt中，执行

    pip3 install -r requirements.txt

    进行类库的下载

主要功能:

    一,输入源采集:

        (-)1,基于流量清洗

        (-)2,基于日志提取

        (+)3,基于爬虫提取

    二,输入源信息搜集(+)

        1,被动信息搜集:(公开渠道可获得信息，与目标系统不产生直接交互)

           (+) 1,whois 信息 获取关键注册人的信息 chinaz

           (+) 2,在线子域名挖掘(这里不会ban掉自身IP，放进被动信息搜集中)

           (+) 3,绕过CDN查找真实IP

           (-) 4,DNS信息搜集

           (+) 5,旁站查询

           (+) 6,指纹识别

           (+) 7,备案信息

            8,搜索引擎搜索

        2,主动信息搜集:

            1,旁站C段服务简单扫描

            2,子域名爆破

            3,敏感目录，文件扫描

            4,端口及运行服务

            5,服务器及中间件信息

            6,WAF检测

            7,敏感信息泄露 .svn,.git 等等

            8,登录界面发现

    三,SQL注入漏洞

    四,XSS漏洞检测

    五,命令执行类漏洞

    六,文件包含类漏洞

    七,登录弱密码爆破

    八,FUZZ模块


可视化界面:

    使用flask+javascript+html+css编写

    启动index.py，在浏览器中访问127.0.0.1:5000访问