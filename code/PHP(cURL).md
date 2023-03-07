# 天气预报查询 - PHP(cURL)调用示例代码

**注意：该示例代码仅适用于 [apispace.com](https://www.apispace.com/?utm_source=github&utm_term=tqcx) 网站下的 API**。

**使用该产品前，您需要通过 [https://www.apispace.com/eolink/api/456456/introduction](https://www.apispace.com/eolink/api/456456/introduction?utm_source=github&utm_term=tqcx) 申请API服务**

### 智能天气实况API
```
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://eolink.o.apispace.com/456456/weather/v001/now?areacode=101010100",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_POSTFIELDS => "",
  CURLOPT_HTTPHEADER => array(
    "X-APISpace-Token:",
    "Authorization-Type:apikey"
  ),
));

$response = curl_exec($curl);

$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```
