# ScrapyCrawler
python爬虫框架scrapy练习
自动爬虫编写总结
单页面爬取思路:
从单页面上爬取链接，利用爬取的链接，设置为初始链接，再创建爬虫进行爬取

关系网：
	爬虫文件依据url开始进行爬取，调用item来进行当前页面所有所需信息的保存，返回item，pipelines获取item，对item的数据进行处理。


1、	在桌面创建文件夹（命名为自动爬取网页）

2、	Cmd命令行，进入自动爬取网页文件夹，创建名为autopjt的scrapy框架项目

cd C:\Users\Administrator\Desktop\自动爬取网页
scrapy startproject autopjt

3、	对autopjt文件夹下的items.py进行编写（定义我们关注的需要爬取的数据）（注，要以最外面的autopjt放到pycharm中打开）
 ![Alt Text](
     https://github.com/appliance/ScrapyCrawler/blob/master/1.png
    )

4、	编写好items.py后，还需要对爬取到的数据做进一步的处理，通过编写pipelines.py文件实现
 ![Alt Text](
     https://github.com/appliance/ScrapyCrawler/blob/master/2.png
    )

5、	编写setting.py文件进行相应的设置

6、	核心部分，爬虫部分的编写
进入autopjt文件，创建一个名为autospd的爬虫文件
scrapy genspider -t basic autospd dangdang.com
 ![Alt Text](
     https://github.com/appliance/ScrapyCrawler/blob/master/3.png
    )

7、需要对爬行网页的url进行观察，发现其中的规律

8、scrapy crawl 爬虫名 执行
