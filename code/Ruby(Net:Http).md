# 天气预报查询 - Ruby(Net:Http)调用示例代码

**注意：该示例代码仅适用于 [apispace.com](https://www.apispace.com/?utm_source=github&utm_term=tqcx) 网站下的 API**。

**使用该产品前，您需要通过 [https://www.apispace.com/eolink/api/456456/introduction](https://www.apispace.com/eolink/api/456456/introduction?utm_source=github&utm_term=tqcx) 申请API服务**

### 智能天气实况API
```
require 'uri'
require 'net/http'

url = URI("https://eolink.o.apispace.com/456456/weather/v001/now?areacode=101010100")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)
request["X-APISpace-Token"] = ""
request["Authorization-Type"] = "apikey"
request.body = ""

response = http.request(request)
puts response.read_body
```
