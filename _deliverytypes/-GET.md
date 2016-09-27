---
title: /deliverytypes
position: 1
type: get
description: Prekių pristatymo būdai
right_code: |
  ~~~ xml
  <?xml version="1.0" encoding="UTF-8"?>
  <response>
    <success>true</success>
    <message></message>
    <items>
      <delivery_type>
        <id>oxdpd</id>
        <title>DPD</title>
        <prices>
          <price>
            <price>0.00</price>
            <price_type>abs</price_type>
            <min_amount>1000.00</min_amount>
            <max_amount>9999999.00</max_amount>
          </price>
          <price>
            <price>20.00</price>
            <price_type>abs</price_type>
            <min_amount>0.00</min_amount>
            <max_amount>1000.00</max_amount>
          </price>
        </prices>
      </delivery_type>
    </items>
  </response>
  ~~~
  {: title="XML" }

  ~~~ json
  {
    "success": true,
    "message": "",
    "items": {
      "delivery_type": [
        {
          "id": "oxdpd",
          "title": "DPD",
          "prices": [
            {
              "price": "0.00",
              "price_type": "abs",
              "min_amount": "1000.00",
              "max_amount": "9999999.00"
            },
            {
              "price": "20.00",
              "price_type": "abs",
              "min_amount": "0.00",
              "max_amount": "1000.00"
            }
          ]
        }
      ]
    }
  }
  ~~~
  {: title="JSON" }

---

Grąžinami esami prekių pristatymo būdai. Ši informacija reikalinga atliekant prekių užsakymą.

oxdpd
: Pristatoma siuntų tarnybos.

oxidstandard
: Atsiėmimas pačiam iš sandėlio.

###### **Atsakymo struktūra(array[DeliveryType])**

| **id** | *string* | Pristatymo identifikatorius |
| **title** | *string* | Pavadinimas |
| **prices** | *array[DeliveryPrice]* | Pristatymo kainos su sąlygomis |
|  |  | **price** (*number*) - Kaina <br>**price_type** (*string*) - Kainos skaičiavimo tipas. Galimos reikšmės: <br>* abs – fiksuota <br>* % - santykinė nuo užsakymo kainos <br>**min_amount** (*number*) - Mažiausia užsakymo kaina nuo kurios taikoma ši atvežimo kaina <br>**max_amount** (*number*) - Didžiausia užsakymo kaina iki kurios taikoma ši atvežimo kaina |