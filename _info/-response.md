---
title: Užklausos grąžinimas
position: 4
right_code: |

  ~~~ xml
  <?xml version="1.0" encoding="UTF-8"?>
  <response>
    <success>true</success>
    <message></message>
    <items>
      <item>
        <attr>value 1</attr>
      </item>
      <item>
        <attr>value 2</attr>
      </item>
    </items>
  </response>
  ~~~
  {: title="XML" }

  ~~~ json
  {
    "success": true,
    "message": "",
    "items": {
      "item": [
        {
          "attr": "value 1"
        },
        {
          "attr": "value 2"
        }
      ]
    }
  }
  ~~~
  {: title="JSON" }
---
Rezultatai grąžinami **XML** (*pagal nutylėjimą*) ir **JSON** formatais.

Išimtinais atvejais gali būti grąžintas **HTML**, tai įvyksta esant klaidai sistemoje.
{: .warning}

Formatą galima nustatyti **HTTP** užklausos antraštėje (*HTTP HEADERS*) – *Accept*.

Galimos reikšmės: *application/json*, *application/xml*.

~~~ bash
curl_setopt($curl,CURLOPT_HTTPHEADER,array('Accept: application/json'));
~~~

Kitas būdas perduoti per **GET** formatą kintamąjame - *_format*. Galimos reikšmės: **JSON, XML**.

~~~
https://api.pretendentas.lt:443/v1/orders?api_key=PRIEIGOS_RAKTAS&_format=json
~~~

| Pavadinimas | Tipas | Pastabos |
| - | - | - |
| success | bool | Nurodo užklausa pavyko (*true*) arba nepavyko (*false*) |
| message | string | Papildoma informacija arba klaidos pranešimas |
| errors | array (optional) | Detalūs klaidos pranešimai |
| items | array(optional) | Grąžinami objektai |