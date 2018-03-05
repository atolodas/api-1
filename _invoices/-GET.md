---
title: /invoices
position: 1
type: get
description: Sąskaitos
right_code: |
  ~~~ xml
  <?xml version="1.0" encoding="UTF-8"?>
  <response>
    <success>true</success>
    <message></message>
    <items>
      <invoice>
        <id>933d65b09a36036a87ae24b01b88e087</id>
        <order_id>4eb7f046bdf4c88013c15e049c0cd3f4</order_id>
        <inv_series></inv_series>
        <inv_nr></inv_nr>
        <res_series>REZ</res_series>
        <res_nr>00001</res_nr>
        <created_at>2013-08-27 11:10:45</created_at>
        <status>UNPAID</status>
        <link_pdf>https://api.pretendentas.lt/v1/invoices/933d65b09a36036a87ae24b01b88e087/download</link_pdf>
        <link_order>https://api.pretendentas.lt/v1/orders/4eb7f046bdf4c88013c15e049c0cd3f4</link_order>
      </invoice>
    </items>
  </response>
  ~~~
  {: title="XML" }

  ~~~ json
  {
    "success": true,
    "message": "",
    "items": {
      "invoice": [
        {
          "id": "933d65b09a36036a87ae24b01b88e087",
          "order_id": "4eb7f046bdf4c88013c15e049c0cd3f4",
          "inv_series": null,
          "inv_nr": null,
          "res_series": "REZ",
          "res_nr": "00001",
          "created_at": "2013-08-27 11:10:45",
          "status": "UNPAID",
          "link_pdf": "https://api.pretendentas.lt/v1/invoices/933d65b09a36036a87ae24b01b88e087/download",
          "link_order": "https://api.pretendentas.lt/v1/orders/4eb7f046bdf4c88013c15e049c0cd3f4"
        }
      ]
    }
  }
  ~~~
  {: title="JSON" }
---
Grąžinama sąskaitų informacija. Sukūrus užsakymą sugeneruojamas rezervacijos numeris (*res_nr*), kai užsakymas patvirtinamas sugeneruojamas išankstinės sąskaitos-faktūros numeris (*inv_nr*).

###### **Atsakymo struktūra(array[Invoice])**

| **id** | *string* | Sąskaitos identifikatorius |
| **order_id** | *string* | Užsakymo, kuriam sugeneruota sąskaita, identifikatorius |
| **inv_series** | *string* | Sąskaitos faktūros serija |
| **inv_nr** | *number* | Sąskaitos faktūros numeris |
| **res_series** | *string* | Išankstinės sąskaitos faktūros serija |
| **res_nr** | *number* | Išankstinės sąskaitos faktūros numeris |
| **created_at** | *string* | Išrašymo laikas |
| **status** | *string* | Būsena. Galimos reikšmės: <br>* PAID – apmokėta <br>* PARTIALLY_PAID - dalinai apmokėta <br>* UNPAID - neapmokėta. |
