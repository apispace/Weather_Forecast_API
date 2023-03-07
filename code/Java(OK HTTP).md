# 天气预报查询 - Java(OK HTTP)调用示例代码

**注意：该示例代码仅适用于 [apispace.com](https://www.apispace.com/?utm_source=github&utm_term=tqcx) 网站下的 API**。

**使用该产品前，您需要通过 [https://www.apispace.com/eolink/api/456456/introduction](https://www.apispace.com/eolink/api/456456/introduction?utm_source=github&utm_term=tqcx) 申请API服务**

### 智能天气实况API
```
OkHttpClient client = new OkHttpClient().newBuilder().build();
MediaType mediaType = MediaType.parse("application/x-www-form-urlencoded");
Request request = new Request.Builder()
  .url("https://eolink.o.apispace.com/456456/weather/v001/now?areacode=101010100")
  .method("GET",null)
  .addHeader("X-APISpace-Token","")
  .addHeader("Authorization-Type","apikey")
  .build();

Response response = client.newCall(request).execute();
```
