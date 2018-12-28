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
![myqr](https://upload-images.jianshu.io/upload_images/13297094-c29f9e3a6671da25.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


#### 饼形图
```
arr = ['袜子','围脖','裤头','手套','帽子']
v = [15,12,45,33,99]
bar = Pie('各商品销售情况')
bar.add("",arr,v,is_stack=True)
bar.render()
```


#### 环形图
```
arr = ['袜子','围脖','裤头','手套','帽子']
v = [15,12,45,33,99]
bar = Pie('饼图-圆环示例图',title_pos='center')
bar.add("",arr,v,radius=[40,75],label_text_color=None,is_label_show=True,legend_orient='vertical',legend_pos='left')
bar.render()
```


#### 散点图
```
v1 = [10,20,30,40,50,60]
v2 = [10,20,30,40,50,60]
scatter = Scatter('散点图示意图')
scatter.add("A",v1,v2)
scatter.add("B",v1[::-1],v2)
scatter.render()
```


#### 仪表盘
```
gauge = Gauge('业务指标完成率-仪表盘')
gauge.add('业务指标','完成率',88.8)
gauge.render()
```


#### 词云图
```
name = ['大数据','AI','Python','医疗','sss','wwww','saz','ssooo']
value = [11,55,33,5,100,600,200,70]
worldcloud = WordCloud(width=1000,height=1000)
worldcloud.add('',name,value,word_size_range=[20,100])
worldcloud.render()
```
