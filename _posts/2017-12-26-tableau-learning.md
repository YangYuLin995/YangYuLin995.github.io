---
layout: article
title:  "Tableau 学习笔记"
date:   2017-12-07 23:55:12 +0800
categories: posts infovis
image:
  teaser: 配图6.jpg
  feature: 配图6.jpg
---
# 美观的可视化需要抓取大量的数据。
---

## 高德地图API
- 高德开放平台提供2D，3D，卫星多种地图形式供开发者选择，无论基于哪种平台，都可以通过高德开放平台提供的API和SDK轻松的完成地图的构建工作。同时我们还提供强大的地图再开发能力，全面的地图数据支持，离线在线两种使用方式，多种地图交互模式，满足各个场景下对地图的需求。

##如何获取API

* 打开百度搜索高德地图官方网站

* 点击注册，注册一个属于自己的账号

* 注册成功后，打开控制台，并且点击应用管理

* 添加新key，点击web服务
### 属于你的api就出现了，利用它在python抓取数据吧！

## 如何抓取数据
### 用python吧！
* 抓取数据，可以使用python编程，将api放入，用jupter自动跑代码，数据很快就出来啦。

### 代码在此

```javascript
  my_api_key = ''
    # amap.com 行政区域查询
# http://lbs.amap.com/api/webservice/guide/api/district/
from pprint import pprint
import requests #用於API HTTP requests
import json     #用於输入出json

# 实践 amap行政区域查询API 中的 服务示例
# http://restapi.amap.com/v3/config/district?keywords=北京&subdistrict=2&key=<用户的key>

url_api = "http://restapi.amap.com/v3/config/district"
parameters = {'keywords': '中国', 
              'subdistrict': 1,
              'key': my_api_key}
r = requests.get (url_api, params=parameters)
data = r.json()
#  dict comprehension code --> int
print( { str(x['adcode']):x['name'] for x in data['districts'][0]['districts'] } )
places = { int(x['adcode']):x['name'] for x in data['districts'][0]['districts'] }
keywords = ['母婴室','残疾人厕所','公共厕所']

import requests #用於API HTTP requests
import pandas as pd


def amap_api_search_by_keyword_city_code(kw, cc, api_key):

    parameters = {'key': api_key}  # 高德地图API 获取Key
    parameters.update( {'keywords': kw,
                        'city':     cc,
                        'citylimit': True
                       } )

    pois = []   # 建构最终结果列表pois
    pg_no = 1   # 建构pg_no，每次给不一样的可选参数page值

    while True: # 不断迭代，直到 break跳出
        parameters.update({'page':pg_no})  #建构可选参数page值 为 pg_no

        r = requests.get ("http://restapi.amap.com/v3/place/text", params=parameters)
        data = r.json()
        #print(data)

        no_pois = int(data['count'])      # 计算 应有的实质数量

        if no_pois>0:
            pois.extend(data.get('pois', []))         # 使用Python列表之extend方法，把返回数据中的结果data['pois']存入pois
            no_pois_this_search = len(pois)   # 计算 累积实质结果数
            if (no_pois_this_search >= no_pois):  # 若 累积实质结果数 >= 应有的实质数量
                break                                   # 则结束迭代跳出
            else:
                pg_no +=1                               # 否则找下一页数据，把 pg_no增1

        else:
            break                                    # empty

    if len(pois)>0:
        # 使用pandas 模块处理数据
        df_input = pd.DataFrame(pois)

        # 选择部份栏位准备输出
        select_fields = ['location', 'address', 'adname', 'cityname', 'id', 'importance', 'name', 'pname', 'tel', 'type', 'typecode']
        df = df_input[select_fields]

        # 经纬度 增加新栏位字段 places 及 keywords
        df = df.assign( 经 = [x.split(',')[0] for x in df['location']])
        df = df.assign( 纬 = [x.split(',')[1] for x in df['location']])
        
        df = df.assign( places_code = [cc]*len(df['location']))
        df = df.assign( places = [places[cc]]*len(df['location']))
        df = df.assign( keywords = [kw]*len(df['location']))
        
    else:
        df = pd.DataFrame([])
    
    # 使用 return返回
    return(df)
    # 全部执行
import os.path
fn_output = "doa.tsv"

for k in keywords:
    for p in places:
        d = amap_api_search_by_keyword_city_code(k, p, my_api_key)
        print ("读取 {地点} 中的 {关键字} 搜索结果...共{几个}个".format(地点=places[p], 关键字=k, 几个=len(d)))

        if os.path.exists(fn_output): 
            header_needed = False
        else:
            header_needed = True
        
        # header  若数据档不存在则输出时包括栏位标题，若已存在则不包括
        d.to_csv(fn_output, encoding='utf8', sep='\t', mode='a',
                                index = False,  index_label=False,
                                header = header_needed)
    
```