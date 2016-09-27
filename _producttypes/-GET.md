---
title: /producttypes
position: 1
type: get
description: Prekių tipai
right_code: |
  ~~~ xml
  <?xml version="1.0" encoding="UTF-8"?>
  <response>
    <success>true</success>
    <message></message>
    <items>
      <product_type>
        <id>899d89984abefc74ac568d1d5515f615</id>
        <title>CLASSIC serija</title>
        <modified_at>2013-07-30 16:18:36</modified_at>
        <active>1</active>
      </product_type>
    </items>
  </response>
  ~~~
  {: title="XML" }

  ~~~ json
  {
    "success": true,
    "message": "",
    "items": {
      "product_type": [
        {
          "id": "899d89984abefc74ac568d1d5515f615",
          "title": "CLASSIC serija",
          "modified_at": "2013-07-30 16:18:36",
          "active": "1"
        }
      ]
    }
  }
  ~~~
  {: title="JSON" }

---
Grąžinami esami prekių tipai. Jų id pateikiami su prekės informacija.

###### **Atsakymo struktūra(array[ProductType])**

| **id** | *string* | Prekės tipo identifikatorius |
| **title** | *string* | Pavadinimas |
| **modified_at** | *string* | Paskutinio koregavimo data ir laikas |
| **active** | *integer* | Aktyvumo būsena. Galimos reikšmės: 0 arba 1 |