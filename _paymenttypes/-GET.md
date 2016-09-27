---
title: /paymenttypes
position: 1
type: get
description: Prekių apmokėjimo būdai
right_code: |
  ~~~ xml
  <?xml version="1.0" encoding="UTF-8"?>
  <response>
    <success>true</success>
    <message></message>
    <items>
      <payment_type>
        <id>oxidinvoice</id>
        <title>Mokėjimas bankiniu pavedimu</title>
        <price>15.00</price>
        <price_type>abs</price_type>
      </payment_type>
    </items>
  </response>

  ~~~
  {: title="XML" }

  ~~~ json
  {
    "success": true,
    "message": "",
    "items": {
      "payment_type": [
        {
          "id": "oxidinvoice",
          "title": "Mokėjimas bankiniu pavedimu",
          "price": "15.00",
          "price_type": "abs"
        }
      ]
    }
  }
  ~~~
  {: title="JSON" }

---
Grąžinami esami užsakymų apmokėjimo būdai. Ši informacija reikalinga atliekant prekių užsakymą.

###### **Atsakymo struktūra(array[PaymentType])**

| **id** | *string* | Prekės tipo identifikatorius |
| **title** | *string* | Pavadinimas |
| **price** | *number* | Kaina |
| **price_type** | *string* | Kainos skaičiavimo tipas. <br>Galimos reikšmės:<br>* abs – fiksuota<br>* % - santykinė nuo užsakymo kainos |
