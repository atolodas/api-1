---
title: /categories/:id/products/extended
position: 4
type: get
description: Prekių sąrašas su papildoma informacija apie prekes nurodytoje kategorijoje
right_code: |
  ~~~ xml
  <?xml version="1.0" encoding="UTF-8"?>
  <response>
    <success>true</success>
    <message></message>
    <items>
      <product>
        <id>278ab94ea088648674ef871ae2838784</id>
        <title>Kavos aparatas Jura IMPRESSA C50</title>
        <artnum>7610917136810</artnum>
        <modified_at>2013-08-06 11:49:46</modified_at>
        <manufacturer_id>c9556a3062a2aaebe14dfe99eff4f862</manufacturer_id>
        <type_id>18c814aadb1282f357b053763d421839</type_id>
        <weight>0</weight>
        <description>
          <![CDATA[<h1><strong>JURA kavos aparatai IMPRESSA C50 -
          "id": "097b73d7db6876b1a16c212467c683df",
          "title": "Kava iš sumaltų kavos pupelių",
          "value": "+"
          Paprastas ir elegantiškas</strong></h1>...]]>
        </description>
        <attributes>
          <attribute>
            <id>85497d1ff1e21d916c819cc8ad2ca671</id>
            <title>Reguliuojamas kavos malūnėlis</title>
            <value>+</value>
          </attribute>
          <attribute>
            <id>097b73d7db6876b1a16c212467c683df</id>
            <title>Kava iš sumaltų kavos pupelių</title>
            <value>+</value>
          </attribute>
        </attributes>
        <pictures>
          <main>
            <nr>1</nr>
            <image>http://b2b.pretendentas.lt/out/pictures/generated/product/1/382_382_75/impressac50black_1.png</image>
          </main>
          <small>
            <image>http://b2b.pretendentas.lt/out/pictures/generated/product/1/76_76_75/impressac50black_1.png</image>
            <image>http://b2b.pretendentas.lt/out/pictures/generated/product/2/76_76_75/impressac50black_2.png</image>
          </small>
          <medium>
            <image>http://b2b.pretendentas.lt/out/pictures/generated/product/1/382_382_75/impressac50black_1.png</image>
            <image>http://b2b.pretendentas.lt/out/pictures/generated/product/2/382_382_75/impressac50black_2.png</image>
          </medium>
          <big>
            <image>http://b2b.pretendentas.lt/out/pictures/generated/product/1/665_665_75/impressac50black_1.png</image>
            <image>http://b2b.pretendentas.lt/out/pictures/generated/product/2/665_665_75/impressac50black_2.png</image>
          </big>
        </pictures>
        <categories_id>
          <id>22b6680935aacc27b1e9b09596644d41</id>
        </categories_id>
      </product>
    </items>
  </response>
  ~~~
  {: title="XML" }

  ~~~ json
  {
    "success": true,
    "message": "",
    "items": {
      "product": [
        {
          "id": "278ab94ea088648674ef871ae2838784",
          "title": "Kavos aparatas Jura IMPRESSA C50",
          "artnum": "7610917136810",
          "modified_at": "2013-08-06 11:49:46",
          "manufacturer_id": "c9556a3062a2aaebe14dfe99eff4f862",
          "type_id": "18c814aadb1282f357b053763d421839",
          "weight": "0",
          "description": "<h1><strong>JURA kavos aparatai IMPRESSA C50 - Paprastas ir elegantiškas<\/strong><\/h1>...",
          "attributes": [
            {
              "id": "85497d1ff1e21d916c819cc8ad2ca671",
              "title": "Reguliuojamas kavos malūnėlis",
              "value": "+"
            },
            {}
          ],
          "pictures": {
            "main": {
              "nr": 1,
              "image": "http://b2b.pretendentas.lt/out/pictures/generated/product/1/382_382_75/impressac50black_1.png"},
              "small": {
                "1": "http://b2b.pretendentas.lt/out/pictures/generated/product/2/76_76_75/impressac50black_1.png",
                "2": "http://b2b.pretendentas.lt/out/pictures/generated/product/2/76_76_75/impressac50black_2.png"
              },
              "medium": {
                "1": "http://b2b.pretendentas.lt/out/pictures/generated/product/2/382_382_75/impressac50black_1.png",
                "2": "http://b2b.pretendentas.lt/out/pictures/generated/product/2/382_382_75/impressac50black_2.png"
              },
              "big": {
                "1": "http://b2b.pretendentas.lt/out/pictures/generated/product/2/665_665_75/impressac50black_1.png",
                "2": "http://b2b.pretendentas.lt/out/pictures/generated/product/2/665_665_75/impressac50black_2.png"
              }
            },
          "categories_id": [
            "22b6680935aacc27b1e9b09596644d41"
          ]
        }
      ]
    }
  }
  ~~~
  {: title="JSON" }
---
Grąžinamas nurodytos kategorijos prekių sąrašas su papildoma informacija apie prekę. Ši informacija keičiasi retai.

###### **Atsakymo struktūra(array[ProductExtended])**

| **id** | *string* | Prekės identifikatorius |
| **title** | *string* | Pavadinimas |
| **artnum** | *string* | Prekės kodas |
| **modified_at** | *string* | Prekės informacijos paskutinio koregavimo data ir laikas |
| **manufacturer_id** | *string* | Gamintojo identifikatorius. Galimų sąrašas: [/manufacturers]({{ site.baseurl }}/#manufacturers-GET) |
| **type_id** | *string* | Prekės tipo identifikatorius. Galimų sąrašas: [/producttypes]({{ site.baseurl }}/#producttypes-GET) |
| **weight** | *double* | Svoris |
| **description** | *string* | Aprašymas, pateikiamas HTML formatu |
| **categories_id** | *array[string]* | Kategorijų id kurioms priskirta prekė |
| **attributes** | *array[attribute]* | Prekės savybės |
| | | **id** (*string*) - Savybė identifikatorius <br>**title** (*string*) - Savybės pavadinimas <br>**value** (*string*) - Savybės reikšmė |
| **pictures** | *ProductImages* | Paveikslėliai |
| | | **main** ProductImageMain  Pagrindinis paveikslėlis <br>* nr (*integer*) - Paveikslėlio numeris <br>** image (*string*) - Paveikslėlio adresas <br>**small** (*array[ProductImage]*) - Mažų dimensijų paveikslėliai <br>* image (*string*) - Paveikslėlio adresas <br>**medium** (*array[ProductImage]*) - Vidutinių dimensijų paveikslėliai <br>* big (*array[ProductImage]*) - Didelių dimensijų paveikslėliai |
