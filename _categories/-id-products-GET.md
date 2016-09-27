---
title: /categories/:id/products
position: 3
type: get
description: Sukurti užsakymą
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
        <manufacturer_id>JURA</manufacturer_id>
        <stock>
          <amount>0</amount>
          <type>inquire</type>
          <delivery>
            <time>2013-10-11</time>
            <unit>date</unit>
          </delivery>
        </stock>
        <price>3799.00</price>
        <old_price></old_price>
        <rmk></rmk>
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
          "manufacturer_id": "JURA",
          "stock": {
            "amount": 0,
            "type": "inquire",
            "delivery": {
              "time": "2013-10-11",
              "unit": "date"
            }
          },
          "price": "3799.00",
          "old_price": null,
          "rmk": null
        }
      ]
    }
  }
  ~~~
  {: title="JSON" }
---
Grąžinamas nurodytos kategorijos bazinis prekių sąrašas. Jo informacija kinta dažnai.

###### **Atsakymo struktūra(array[Product])**

| **id** | *string* | Prekės identifikatorius |
| **title** | *string* | Pavadinimas |
| **artnum** | *string* | Prekės kodas |
| **modified_at** | *string* | Prekės informacijos paskutinio koregavimo data ir laikas |
| **manufacturer_id** | *string* | Gamintojo identifikatorius. Galimų sąrašas: [/manufacturers]({{ site.baseurl }}/#manufacturers-GET) |
| **stock** | *Stock* | Kiekis |
| | | **type** (*string*) - Kiekio tipas. Galimos reikšmės: <br>* morethan - turima daugiau nei nurodyta <br>* total - tikslus skaičius <br>* orderable - specialiai užsakoma <br>* inquire - teirautis dėl likučio <br>**amount** (*double*) - Prekės kiekis <br>**delivery** (*DeliveryTime*) - Pristatymo laikas <br>* time (*string*) - Jei tipas *orderable*, tai *time* nurodo per kiek laiko bus pristatyta prekė, ją užsakius. Kitu atveju, konkreti data (*unit - date*) <br>* unit (*string*) - Pristatymo laiko matas *time* laukui. Galimos reikšmės: <br>** day – dienomis <br>** week – savaitėmis <br>** month – mėnesiais <br>** date - konkreti data(jei *time* ne orderable). |
| **price** | *number* | Kaina |
| **old_price** | *number* | Buvusi kaina, jei prekei taikoma nuolaida |
| **rmk** | *number* | Rekomenduojama mažmeninė kaina |
