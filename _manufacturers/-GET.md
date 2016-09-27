---
title: /manufacturers
position: 1
type: get
description: Prekių gamintojų pavadinimai
right_code: |
  ~~~ xml
  <?xml version="1.0" encoding="UTF-8"?>
  <response>
    <success>true</success>
    <message></message>
    <items>
      <manufacturer>
        <id>72fea404c5a68a13f6e5eb9b4a366081</id>
        <title>ADLER</title>
        <description/>
        <modified_at>2013-10-28 16:46:39</modified_at>
        <active>1</active>
      </manufacturer>
    </items>
  </response>
  ~~~
  {: title="XML" }

  ~~~ json
  {
    "success": true,
    "message": "",
    "items": {
      "manufacturer": [
        {
          "id": "72fea404c5a68a13f6e5eb9b4a366081",
          "title": "ADLER",
          "description": "",
          "modified_at": "2013-10-28 16:46:39",
          "active": "1"
        }
      ]
    }
  }

  ~~~
  {: title="JSON" }

---
Grąžinamas esamų prekių gamintojų sąrašas. Jų id pateikiami su prekės informacija.

###### **Atsakymo struktūra(array[Manufacturer])**

| **id** | *string* | Prekės tipo identifikatorius |
| **title** | *string* | Pavadinimas |
| **description** | *string* | Aprašymas, pateikiamas HTML formatu |
| **modified_at** | *string* | Paskutinio koregavimo data ir laikas |
| **active** | *integer* | Aktyvumo būsena. Galimos reikšmės: 0 arba 1 |