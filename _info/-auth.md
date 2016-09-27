---
title: Identifikacija
position: 3
right_code: |
  ~~~ javascript
  $.get("https://api.pretendentas.lt:443/v1/orders", { "api_key": "PRIEIGOS_RAKTAS"}, function(data) {
    alert(data);
  });
  ~~~
  {: title="jQuery" }

  ~~~ python
  r = requests.get("https://api.pretendentas.lt:443/v1/orders?api_key=PRIEIGOS_RAKTAS")
  print r.text
  ~~~
  {: title="Python" }

  ~~~ javascript
  var request = require("request");
  request("https://api.pretendentas.lt:443/v1/orders?api_key=PRIEIGOS_RAKTAS", function (error, response, body) {
    if (!error && response.statusCode == 200) {
      console.log(body);
    }
  });
  ~~~
  {: title="Node.js" }

  ~~~ bash
  curl https://api.pretendentas.lt:443/v1/orders?api_key=PRIEIGOS_RAKTAS
  ~~~
  {: title="Curl" }
---
Identifikacija atliekama pagal prieigos raktą (*API key*).
Rekomenduojama nustatyti **HTTP** užklausos antraštėje (*HTTP headers*) – **API-KEY**.

Duomenys nebus grąžinti, jei nebus nustatytas **API-KEY**
  {: .error }

~~~
curl_setopt($curl,CURLOPT_HTTPHEADER,array('api-key: PRIEIGOS_RAKTAS'));
~~~

Testuojant galima perduoti per **GET**.

~~~
https://api.pretendentas.lt:443/v1/orders?api_key=PRIEIGOS_RAKTAS
~~~
