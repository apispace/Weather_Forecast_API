# APISpace 介绍
**本 API 服务由 [APISpace（apispace.com）](https://www.apispace.com/?utm_source=github&utm_term=tqcx) 提供。**

APISpace 是 Eolink 旗下专业的 API 开放与交易平台，为广大企业以及个人开发者提供多维度、全方位的API接口，覆盖短信验证、天气查询、快递物流、OCR文字识别等海量 API 服务，帮助用户快速获取数据，降低获取数据的成本和难度，提升开发效率。
# 天气预报查询
支持全国以及全球多个城市的天气查询，包含国内3400+个城市以及国际4万个城市的实况数据；更新频率分钟级别。

**使用该产品前，您需要通过 [https://www.apispace.com/eolink/api/456456/introduction](https://www.apispace.com/eolink/api/456456/introduction?utm_source=github&utm_term=tqcx) 申请API服务**

本文档提供 **天气预报查询服务** 的 **智能天气实况API** 的各种开发语言的调用代码示例，具体请查看code文件夹。

**该产品拥有以下APIs：**
1. 智能天气实况
2. 天气逐小时预报
3. 天气逐3小时预报
4. 15天预报
5. 城市搜索（支持国内、国外城市）

### API列表
#### 1. 智能天气实况 API
- 天气实况是天气预报中最基础的数据，主要是对最近天气进行的监测，该接口的更新频率是分钟级。
- 支持国内3400+个城市以及国际4万个城市的实况数据。

#### 2. 天气逐小时预报 API
- 提供全球城市长达72小时的逐时预报，包含天气现象、气温、体感温度、风力、风向、相对湿度、云量、1小时降水量等。
- 支持国内3400+个城市以及国际4万个城市的预报数据。


#### 3. 天气逐3小时预报 API
- 提供长达7天的逐3小时预报，包含天气现象、气温、体感温度、风力、风向、相对湿度、云量、降水量等。
- 支持国内3400+个城市的预报数据。


#### 4. 15天预报 API
- 提供长达15天的天气预报，具体要素包含：将一个自然日区分为白天、黑夜，分别预报出天气现象、最高气温、最低气温、风力、风向等。
新增了白天风速、白天风向角度、白天云量、夜间风速、夜间风向角度、夜间云量、最大相对湿度、最小相对湿度、降水概率、气压、能见度、紫外线指数等要素。
- 支持国内3400+个城市以及国际4万个城市的预报数据。


#### 5.  国内/国外城市查询 API
用于获取请求参数 **areacode:城市ID** 

- 可根据城市中文名、英文名或拼音，检索匹配全球的城市信息。
- 支持模糊搜索，可指定搜索范围（中国或全球），设置返回结果数量等。
- 支持中国31个省、直辖市、自治区及港澳台地区共3400+个城市的地理信息；支持全球200多个国家和地区共39474个城市的地理信息。

### 相关附件
- [点击查看国内城市_3405站](https://easy-open-link.feishu.cn/wiki/wikcnXfeZ1lmUCbCSac2hYAEFb2)
- [点击查看国际城市_39474站](https://easy-open-link.feishu.cn/wiki/wikcn4Xysjpxc2YvMPWaIRtorlG)
- [天气状态编码表](https://easy-open-link.feishu.cn/wiki/wikcnvz05NuYDNZQswrQgixdj1b)


### 返回示例
以智能天气实况为例
```
{
    “status”: 0,
    “result”: {
        “location”: {
            “areacode”: “JPN10041001001”,    //城市ID
            “name”: “足立区”,            //城市中文名
            “country”: “日本”,            //所属国家中文名
            “path”: “足立区,足立区,东京都,日本”    //行政区划路径
        },
        “realtime”: {
            “text”: “多云”,        //天气现象，string类型
            “code”: “01”,            //天气现象编码，string类型
            “temp”: 6.5,            //气温，单位℃，double类型
            “feels_like”: 6,        //体感温度，单位℃，int类型
            “rh”: 38,            //相对湿度，单位%，int类型
            “wind_class”: “2级”,        //蒲福氏风级，string类型
            “wind_speed”: 2.5,    //风速，单位m/s，double类型
            “wind_dir”: “南风”,        //风向，string类型
            “wind_angle”: 187,    //风向角度，0表示正北，180表示正南，int类型
            “prec”: 0.0,            //过去1小时降水量，单位毫米(mm)，double类型
            “clouds”: 99,        //云量，单位%，int类型
            “vis”: 12085,        //能见度，单位米(m)，int类型
            “pressure”: 1020,        //气压，单位百帕(hPa)，int类型
            “dew”: -6,            //露点温度，单位℃，int类型
            “uv”: 2,            //紫外线指数，int类型
            “snow”: 0.0,        //降雪量，单位厘米(cm)，double类型 #国内城市不支持#
            “weight”: 0,        //文案权重，int类型
            “brief”: “今日惊蛰”,        //天气短文案，string类型
            “detail”: “今日惊蛰，春雷惊百虫”,        //天气长文案 ，string类型
        },
        “last_update”: “2021-03-05 19:07:44”    //数据更新时间(北京时间)
    }
}
```

### 产品优势
![image](https://user-images.githubusercontent.com/36323798/223364839-44ffc9d8-7d45-40bd-93b2-d0075c4f5264.png)

### 服务保障
![image](https://user-images.githubusercontent.com/36323798/223365050-2a81fcd2-69af-46b9-bb61-1fdc97faf768.png)

