---
title: /categories
position: 1
type: get
description: Kategorijų medis
right_code: |
  ~~~ xml
  <?xml version="1.0" encoding="UTF-8"?>
  <response>
  <success>true</success>
  <message></message>
  <items>
  <category>
    <id>30511f0090ee14ab0557d099ef159482</id>
    <title>Kavos aparatai / priedai ir priežiūra</title>
    <description/>
    <short_description/>
    <products_count>0</products_count>
    <subcategories>
      <category>
      <id>22b6680935aacc27b1e9b09596644d41</id>
      <title>- Kavos aparatai namams</title>
      <description/>
      <short_description/>
      <products_count>22</products_count>
      </category>
    </subcategories>
  </category>
  </items>
  </response>
  ~~~
  {: title="XML" }

  ~~~ json
  {
    "success": true,
    "message": "",
    "items": {
      "category": [
        {
          "id": "30511f0090ee14ab0557d099ef159482",
          "title": "Kavos aparatai / priedai ir priežiūra",
          "description": null,
          "short_description": "",
          "products_count": "0",
          "subcategories": [
            {
              "id": "22b6680935aacc27b1e9b09596644d41",
              "title": "- Kavos aparatai namams",
              "description": null,
              "short_description": "",
              "products_count": "22"
            }
          ]
        }
      ]
    }
  }
  ~~~
  {: title="JSON" }
---

Grąžinamas prekių kategorijų medis.

###### **Atsakymo struktūra(array[Category])**

| **id** | *string* | Kategorijos identifikatorius |
| **title** | *string* | Pavadinimas |
| **description** | *string* | Aprašymas, pateikiamas HTML formatu |
| **short_description** | *string* | Aprašo santrumpa |
| **products_count** | *integer* | Šiai kategorijai priskirtų prekių skaičius |
| **subcategories** | *array[Category]* | Kategorijos subkategorijos. Struktūra tokia pati |