---
title: /user
position: 1.0
type: get
description: Vartotojo informacija
right_code: |

  ~~~ xml
  <?xml version="1.0" encoding="UTF-8"?>
  <response>
      <success>true</success>
      <message></message>
      <items>
          <user>
              <id>test_user</id>
              <username>test@example.com</username>
              <customer_number>1111</customer_number>
              <company>Testing lab</company>
              <firstname>Tester</firstname>
              <lastname>User</lastname>
              <credit>20000</credit>
              <used_credit>100.0</used_credit>
              <addresses>
                  <address>
                      <id>main</id>
                      <street>Bleeding edge</street>
                      <street_nr>1</street_nr>
                      <city>Kaunas</city>
                      <zip>LT5000</zip>
                      <firstname>Tester</firstname>
                      <lastname>User</lastname>
                      <company>Testing lab</company>
                      <phone>+37011111111</phone>
                  </address>
              </addresses>
          </user>
      </items>
  </response>
  ~~~
  {: title="XML" }

  ~~~ json
  {
    "success": true,
    "message": "",
    "items": {
      "user": {
        "id": "test_user",
        "username": "test@example.com",
        "customer_number": "1111",
        "company": "Testing lab",
        "firstname": "Tester",
        "lastname": "User",
        "credit": 20000,
        "used_credit": 100.0,
        "addresses": [
          {
            "id": "main",
            "street": "Bleeding edge",
            "street_nr": "1",
            "city": "Kaunas",
            "zip": "LT5000",
            "firstname": "Tester",
            "lastname": "User",
            "company": "Testing lab",
            "phone": "+37011111111"
          }
        ]
      }
    }
  }
  ~~~
  {: title="JSON" }

---
Grąžinama **API** vartotojo informacija. Grąžinami adresai gali būti naudojami nurodant užsakyme prekių pristatymo vietą.

###### **Atsakymo struktūra(User)**

| **id** | *string* | Vartotojo identifikatorius |
| **username** | *string* | Prisijungimo vardas |
| **customer_number** | *string* | Pirkėjo numeris |
| **company** | *string* | Įmonės pavadinimas |
| **firstname** | *string* | Vardas |
| **lastname** | *string* | Pavardė |
| **credit** | *number* | Suteiktas kreditas |
| **used_credit** | *number* | Nupirktų prekių į kreditą suma |
| **addresses** | *array[Address]* | Pristatymo adresų informacija |
| | | **id** (*string*) - Adreso identifikatorius, naudojamas užsakyme nurodyti pristatymo adresą <br>**street** (*string*) - Gatvės pavadinimas <br>**street_nr** (*string*) - Namo numeris, daugiausiai 16 ženklų <br>**city** (*string*) - Miesto/gyvenvietės pavadinimas <br>**zip** (*string*) - Pašto kodas <br>**firstname** (*string*) - Kontaktinio asmens vardas <br>**lastname** (*string*) - Kontaktinio asmens pavardė <br>**company** (*string*) - Įmonės pavadinimas <br>**phone** (*string*) - Kontaktinis telefono numeris |