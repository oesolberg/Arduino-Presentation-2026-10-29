# Arduino Presentation Oct 2026

**Hjemmelaget automatikk:** sju prosjekter med Arduino, ESP32 og Netduino i hus, hage og drivhus.

En kort fagprat (5–10 minutter) for IT-kolleger om små mikrokontrollere som måler, bestemmer og styrer ting hjemme, og hvordan alt henger sammen i HomeSeer.

## Filer

| Fil | Innhold |
| --- | --- |
| `Arduino-Presentation-Oct-2026.pdf` | Presentasjonen som PDF |
| `Arduino-Presentation-Oct-2026.pptx` | Presentasjonen som PowerPoint, med talenotater |

## Prosjektene

| # | Prosjekt | Kort | Kommunikasjon |
| --- | --- | --- | --- |
| 1 | Vanning av mais i kjelleren | Netduino (C#) | Ingen, jobbet alene |
| 2 | Viftestyring i stereobenk | ESP32 | MQTT til HomeSeer |
| 3 | Viftestyring i serverskap | ESP32 | MQTT til HomeSeer |
| 4 | Viftestyring i drivhuset | ESP32 | UDP til HomeSeer |
| 5 | Vanning av hagen med Gardena-ventiler | Z-Uno | Z-Wave til HomeSeer |
| 6 | Brannvarsler-sensor | Z-Uno | Z-Wave til HomeSeer |
| 7 | Temperaturmåling i jorda | ESP32 FireBeetle | UDP til HomeSeer |

### Kort fortalt

- **Maisvanning:** To metallfølere melder tomt og fullt reservoar. Pumpen går i pulser på 10 sekunder til reservoaret er fullt.
- **Stereobenk og serverskap:** DS18B20-føler, relé og vifter. Hysterese hindrer at viftene går av og på hele tiden: 40/34 °C i stereobenken og 35/32 °C i serverskapet.
- **Drivhus:** To vifter på 220 V AC styres med releer og henter kjøligere luft fra nordsiden. Fem trinn fra 26 til 34 °C.
- **Gardena:** Seks vanningspunkter. Ecowitt-fuktsensorer leses inn i HomeSeer, som bestemmer når det skal vannes. Z-Uno slår releer til 24 V AC-ventiler og sender status tilbake.
- **Brannvarsler:** Alarmsignal fra et relékort leses av Z-Uno. HomeSeer sender SMS og slår på lys i soverom og ganger.
- **Jordtemperatur:** Fire DS18B20-følere på 10, 20, 50 og 100 cm dybde, drevet av batterier og solcelle. Sender data omtrent hvert 30. minutt. All koden er skrevet av Claude.

## Bilder

Netduino-bildet er fra Wikimedia Commons (`And_the_ARM_core.jpg`). ESP32-bildet er fra Joy-IT, og Z-Uno-bildet er fra Hackmag. De øvrige bildene er egne.