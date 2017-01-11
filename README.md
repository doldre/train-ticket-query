# 12306余票查询
自动访问12306抓取余票数据，若有余票将发送邮件

使用帮助（数据库版）：

1. 在数据库新建trainquery库和querylist表，表结构见sql文件

2. 运行python add_queriers.py可以往数据库添加待查询的车次
	参数说明：
	* -h 帮助
	* -f 必选参数，出发地，例如：福州
	* -t 必选参数，目的地，例如：杭州
	* -d 必选参数，日期，格式：2017-01-20
	* -n 可选参数，指定车次，逗号分隔，例如：D3343,G366
	* -s 可选参数，指定坐席，逗号分隔，例如：二等座，无座
	示例：
	python add_queriers.py -f 福州 -t 杭州 -d 2017-01-20

3. 运行python 12306.py即可读取数据库，在后台默默轮询查票了

其他，配置项基本都在config.py

