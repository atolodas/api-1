---
title: Klaidos
position: 5
---
Klaidas galima identifikuoti pagal grąžinamas reikšmes.

Jei *success = false*, žinutėje (*message*) nurodomas bendras klaidos aprašymas.

Kartais detalesnė reikšmė gali būti pateikiama errors masyve.

Taip pat klaidas galima identifikuoti pagal **HTTP** atsako kodą (*HTTP Status Code*).


| Kodas | Aprašymas |
|-------|-----------------------------------|
| 400   | Neteisinga užklausa               |
| 403   | Nepakanka teisių, nenurodytas prieigos raktas arba jis neteisingas |
| 404   | Nerastas užsiprašytas resuras     |
