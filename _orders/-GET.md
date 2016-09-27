---
title: /orders
position: 1
type: get
description: Užsakymų sąrašas
right_code: |
  ~~~ xml
  <?xml version="1.0" encoding="UTF-8"?>
  <response>
    <success>true</success>
    <message></message>
    <items>
      <order>
        <id>f40292e001cfe4fef189265a0f70d7da</id>
        <created_at>2013-08-13 14:09:01</created_at>
        <order_nr>4</order_nr>
        <bill_company>Testing lab</bill_company>
        <bill_firstname>Tester</bill_firstname>
        <bill_lastname>User</bill_lastname>
        <bill_additional_info></bill_additional_info>
        <total_netto>1980</total_netto>
        <total_bruto>2395.8</total_bruto>
        <total_order_sum>2415.8</total_order_sum>
        <vat_type>21</vat_type>
        <vat_amount>415.8</vat_amount>
        <currency>LTL</currency>
        <delivery_company></delivery_company>
        <delivery_firstname>Delivering</delivery_firstname>
        <delivery_lastname>Tester</delivery_lastname>
        <delivery_street>Far Away.</delivery_street>
        <delivery_street_nr>42</delivery_street_nr>
        <delivery_city>Universe</delivery_city>
        <delivery_zip>LT-52000</delivery_zip>
        <delivery_phone>+37060000000</delivery_phone>
        <delivery_additional_info></delivery_additional_info>
        <delivery_type>dpd</delivery_type>
        <delivery_date>2013.08.14</delivery_date>
        <delivery_time>0_12</delivery_time>
        <modified_at>2013-09-26 16:35:53</modified_at>
      </order>
    </items>
  </response>
  ~~~
  {: title="XML" }

  ~~~ json
  {
    "success": true,
    "message": "",
    "items": {
      "order": [
        {
          "id": "f40292e001cfe4fef189265a0f70d7da",
          "created_at": "2013-08-13 14:09:01",
          "order_nr": "4",
          "bill_company": "Testing lab",
          "bill_firstname": "Tester",
          "bill_lastname": "User",
          "bill_additional_info": "",
          "total_netto": "1980",
          "total_bruto": "2395.8",
          "total_order_sum": "2415.8",
          "vat_type": "21",
          "vat_amount": "415.8",
          "currency": "LTL",
          "delivery_company": "",
          "delivery_firstname": "Delivering",
          "delivery_lastname": "Tester",
          "delivery_street": "Far Away.",
          "delivery_street_nr": "2",
          "delivery_city": "Universe",
          "delivery_zip": "LT-52000",
          "delivery_phone": "+37060000000",
          "delivery_additional_info": "",
          "delivery_type": "dpd",
          "delivery_date": "2013.08.14",
          "delivery_time": "0_12",
          "modified_at": "2013-09-26 16:35:53"
        }
      ]
    }
  }
  ~~~
  {: title="JSON" }
---
Grąžinamas vartotojo visų užsakymų sąrašas.

###### **Atsakymo struktūra(array[OrderInfo])**

| **id** | *string* | Užsakymo identifikatorius |
| **created_at** | *string* | Užsakymo sukūrimo laikas |
| **order_nr** | *integer* | Užsakymo numeris |
| **bill_company** | *string* | Mokėtojo(juridinio asmens) pavadinimas |
| **bill_firstname** | *string* | Mokėtojo vardas |
| **bill_lastname** | *string* | Mokėtojo pavardė |
| **bill_additional_info** | *string* | Papildoma mokėjimo informacija, pastabos |
| **total_netto** | *integer* | Prekių suma (*be PVM*) |
| **total_bruto | *integer* | Prekių suma (*su PVM*) |
| **total_order_sum** | *integer* | Užsakymo bendra suma |
| **vat_type** | *integer* | PVM tipas |
| **vat_amount** | *integer* | PVM suma |
| **currency** | *string* | Valiuta |
| **delivery_company** | *string* | Įmonės pavadinimas, jei gavėjas yra juridinis asmuo |
| **delivery_firstname** | *string* | Vardas, jei gavėjas yra fizinis asmuo |
| **delivery_lastname** | *string* | Pavardė, jei gavėjas yra fizinis asmuo |
| **delivery_street** | *string* | Pristatymo gatvė |
| **delivery_street_nr** | *string* | Pristatymo namo numeris |
| **delivery_city** | *string* | Pristatymo miestas |
| **delivery_zip** | *string* | Pristatymo pašto kodas |
| **delivery_phone** | *string* | Gavėjo kontaktinis telefonas |
| **delivery_additional_info** | *string* | Papildoma pristatymo informacija, pastabos |
| **delivery_type** | *string* | Pristatymo tipas. Galimi pristatymo tipai: [/deliverytypes]({{ site.baseurl }}/#deliverytypes-GET) |
| **delivery_date** | *string* | Numatoma pristatymo data |
| **delivery_time** | *string* | Numatomas pristatymo laikas |
| **modified_at** | *string* | Užsakymo informacijos atnaujinimo data |
