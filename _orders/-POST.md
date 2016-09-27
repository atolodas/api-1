---
title: /orders
position: 2
type: post
description: Sukurti užsakymą
---
Prekių užsakymas vykdomas siunčiant **POST** užklausą, kurioje order reikšmė yra užsakymo informacija. Alternatyvus būdas yra siųsti **POST** užklausą su užsakymo informacija **JSON** formatu.
Jei prekės pristatomos per kurjerių tarnybą (*delivery_type - oxdpd*) privaloma užsakyme pateikti gavėjo adresą. Jis gali būti nurodomas iš vartotojo adresų (*žiūrėti: [/user](/#user-GET)*) *delivery_address_id* laukelyje arba įvestas tam skirtuose laukeliuose.

~~~
https://api.pretendentas.lt/v1/examples/order
~~~

| **delivery_type** | *string* | Pristatymo būdas. Galimi būdai: [/deliverytypes](/#deliverytypes-GET) |
| **bill_payment_type** | *string* | Apmokėjimo būdas. Galimi apmokėjimai: [/paymenttypes](/#paymenttypes-GET) |
| **products** | *array[OrderProduct]* | Užsakomos prekės |
| | | **id** (*string*) - Prekės id <br>**quantity** (*integer*) - Užsakomas kiekis |
| **bill_additional_info** | *string, optional* | Papildoma mokėjimo informacija, pastabos |
| **delivery_additional_info** | *string, optional* | Papildoma pristatymo informacija, pastabos |
| **delivery_address_id** | *integer, optional* | Pristatymo adreso id. Galimi pristatymo adresai: [/user](/#user-GET). Nurodomas adreso id arba užpildomi žemiau esantys pristatymo laukai |
| **delivery_company** | *string, optional* | Įmonės pavadinimas, jei gavėjas yra juridinis asmuo |
| **delivery_firstname** | *string, optional* | Vardas, jei gavėjas yra fizinis asmuo |
| **delivery_lastname** | *string, optional* | Pavardė, jei gavėjas yra fizinis asmuo |
| **delivery_street** | *string, optional* | Pristatymo gatvė |
| **delivery_street_nr** | *string, optional* | Pristatymo namo numeris |
| **delivery_city** | *string, optional* | Pristatymo miestas |
| **delivery_zip** | *string, optional* | Pristatymo pašto kodas |
| **delivery_phone** | *string, optional* | Gavėjo kontaktinis telefonas |


###### **Užsakymo siuntimo realizacija (php)**
Užkomentuota dalis realizuoja alternatyvų duomenų perdavimą JSON formatu.

~~~ php
<?php
$apiKey = "YOUR_API_KEY";

$availableEncoding = array('application/json', 'application/xml');
$encoding = $availableEncoding[0];

$order = array(
    'delivery_type' => 'oxdpd', // /deliverytypes
    'bill_payment_type' => 'oxidinvoice', // /paymenttypes
    'products' => array(
        array(
            'id' => '043e8b764a52ba88bf5743b8aa489ac0',
            'quantity' => 1,
        ),
     ),

    'delivery_address_id' => 'main', // /user
    'bill_additional_info' => 'payment will delay few hours',
    'delivery_company' => 'Test company',
    'delivery_firstname' => 'Beta',
    'delivery_lastname' => 'Testing',
    'delivery_street' => 'Area',
    'delivery_street_nr' => '52',
    'delivery_city' => 'Desert',
    'delivery_zip' => 'LT-46532',
    'delivery_phone' => '+123456789',
    'delivery_additional_info' => 'please deliver as fast as you can',
);


$postContent = http_build_query(array('order' => $order));
//$postContent = json_encode($order);

$curl = curl_init();
$encoding = array('application/json', 'application/xml');

curl_setopt($curl,CURLOPT_HTTPHEADER,array(
    'Accept: '. $encoding[0],
    'api-key: '. $apiKey,
//    'Content-Type: application/json',
//    'Content-Length: ' . strlen($post_string),
));
curl_setopt($curl, CURLOPT_URL,"https://api.pretendentas.lt/v1/orders/create");
curl_setopt($curl, CURLOPT_POST, 1);
curl_setopt($curl, CURLOPT_POSTFIELDS, $postContent);
curl_setopt($curl, CURLOPT_RETURNTRANSFER, true);

$output = curl_exec ($curl);
curl_close ($curl);

$response = json_decode($output);
var_dump($response);
~~~
{: title="php" }