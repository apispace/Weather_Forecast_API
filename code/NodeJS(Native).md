# 天气预报查询 - NodeJS(Native)调用示例代码

**注意：该示例代码仅适用于 [apispace.com](https://www.apispace.com/?utm_source=github&utm_term=tqcx) 网站下的 API**。

**使用该产品前，您需要通过 [https://www.apispace.com/eolink/api/456456/introduction](https://www.apispace.com/eolink/api/456456/introduction?utm_source=github&utm_term=tqcx) 申请API服务**

### 智能天气实况API
```
var qs = require("querystring");
var http = require("https");
var requestInfo={
    "method": "GET",
    "hostname": "eolink.o.apispace.com",
    "path": "/456456/weather/v001/now?areacode=101010100",
    "headers": {
        "X-APISpace-Token":"",
        "Authorization-Type":"apikey"
   }
};

var req = http.request(requestInfo, function (res) {
    var chunks = [];

    res.on("data", function (chunk) {
        chunks.push(chunk);
    });

    res.on("end", function () {
        var body = Buffer.concat(chunks);
        console.log(body.toString());
    });
});

req.write(qs.stringify({

}));
req.end();
```
