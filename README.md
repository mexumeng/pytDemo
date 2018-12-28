## Demo1 
### python的报表模块练习
#### 导入模块


```
#!/usr/bin/env python
# -*- coding: utf-8 -*-
__author__ = "xumeng"
__date__ = "2018/12/27 22:45"
from pyecharts import Bar,Pie,Scatter,Gauge,WordCloud
```


#### 直方图
```
arr = ['袜子','围脖','裤头','手套','帽子']
v1 = [15,12,45,33,99]
v2 = [10,2,88,33,74]
bar = Bar('各商家商品销售情况')
bar.add("商家A",arr,v1,is_stack=True)
bar.add("商家B",arr,v2,is_stack=True)
bar.render()
```
![myqr](http://pjwvkfdq5.bkt.clouddn.com/%E5%90%84%E5%95%86%E5%AE%B6%E5%95%86%E5%93%81%E9%94%80%E5%94%AE%E6%83%85%E5%86%B5.png)


#### 饼形图
```
arr = ['袜子','围脖','裤头','手套','帽子']
v = [15,12,45,33,99]
bar = Pie('各商品销售情况')
bar.add("",arr,v,is_stack=True)
bar.render()
```
![myqr](http://pjwvkfdq5.bkt.clouddn.com/%E5%90%84%E5%95%86%E5%93%81%E9%94%80%E5%94%AE%E6%83%85%E5%86%B5.png)


#### 环形图
```
arr = ['袜子','围脖','裤头','手套','帽子']
v = [15,12,45,33,99]
bar = Pie('饼图-圆环示例图',title_pos='center')
bar.add("",arr,v,radius=[40,75],label_text_color=None,is_label_show=True,legend_orient='vertical',legend_pos='left')
bar.render()
```
![myqr](http://pjwvkfdq5.bkt.clouddn.com/%E9%A5%BC%E5%9B%BE-%E5%9C%86%E7%8E%AF%E7%A4%BA%E4%BE%8B%E5%9B%BE.png)


#### 散点图
```
v1 = [10,20,30,40,50,60]
v2 = [10,20,30,40,50,60]
scatter = Scatter('散点图示意图')
scatter.add("A",v1,v2)
scatter.add("B",v1[::-1],v2)
scatter.render()
```
![myqr](http://pjwvkfdq5.bkt.clouddn.com/%E6%95%A3%E7%82%B9%E5%9B%BE%E7%A4%BA%E6%84%8F%E5%9B%BE.png)


#### 仪表盘
```
gauge = Gauge('业务指标完成率-仪表盘')
gauge.add('业务指标','完成率',88.8)
gauge.render()
```
![myqr](http://pjwvkfdq5.bkt.clouddn.com/%E4%B8%9A%E5%8A%A1%E6%8C%87%E6%A0%87%E5%AE%8C%E6%88%90%E7%8E%87\-%E4%BB%AA%E8%A1%A8%E7%9B%98.png)


#### 词云图
```
name = ['大数据','AI','Python','医疗','sss','wwww','saz','ssooo']
value = [11,55,33,5,100,600,200,70]
worldcloud = WordCloud(width=1000,height=1000)
worldcloud.add('',name,value,word_size_range=[20,100])
worldcloud.render()
```
![myqr](http://pjwvkfdq5.bkt.clouddn.com/%E8%AF%8D%E4%BA%91%E5%9B%BE.png)
