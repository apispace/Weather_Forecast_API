# 天气预报查询 - PHP(pecl_http)调用示例代码

**注意：该示例代码仅适用于 [apispace.com](https://www.apispace.com/?utm_source=github&utm_term=tqcx) 网站下的 API**。

**使用该产品前，您需要通过 [https://www.apispace.com/eolink/api/456456/introduction](https://www.apispace.com/eolink/api/456456/introduction?utm_source=github&utm_term=tqcx) 申请API服务**

#### 智能天气实况 API
```
<?php

$client = new http\Client;
$request = new http\Client\Request;

$body = new http\Message\Body;
$body->append(new http\QueryString(array({

))));

$request->setRequestUrl("eolink.o.apispace.com/456456/weather/v001/now");
$request->setRequestMethod("GET");
$request->setBody($body);

$request->setQuery(new http\QueryString(array(
  "areacode" => "101010100"
)));

$request->setHeaders(array(
  "X-APISpace-Token" => "",
  "Authorization-Type" => "apikey"
));

$client->enqueue($request)->send();
$response = $client->getResponse();

echo $response->getBody();
```
