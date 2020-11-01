# The Thing Network (TTN)

1. "Sign Up"

![TTN1](Pictures_TTN/Screenshot_20201025_092149.png)

2. Nutzername, Email-Adresse und Passwort eingeben. Mit "Create account" bestätigen

![TTN1](Pictures_TTN/Screenshot_20201028_191334.png)

3. Ist der Account angelegt, muss man auf die Bestätigungsmail warten.

![TTN1](Pictures_TTN/Screenshot_20201028_191348.png)

4. Im Email-Postfach "Activate account" klicken.

![TTN1](Pictures_TTN/Screenshot_20201028_191552.png)

5. Den Reiter "Console" auswählen.

![TTN1](Pictures_TTN/Screenshot_20201028_191634.png)

6. "Applications" auswählen.

![TTN1](Pictures_TTN/Screenshot_20201028_191858.png)

7. Mit "Get started by adding one!" oder "+ add application" eine Application anlegen.

![TTN1](Pictures_TTN/Screenshot_20201028_191915.png)

8. Application ID und Description vergeben und mit "Add application" bestätigen.

![TTN1](Pictures_TTN/Screenshot_20201028_192029.png)

9. "+ register device" auswählen.

![TTN1](Pictures_TTN/Screenshot_20201028_192102.png)

10. Device ID vergeben und mit "Register" bestätigen.

![TTN1](Pictures_TTN/Screenshot_20201028_192147.png)

11. Die nun angezeigten Daten müssen in die Sensorfirmware übernommen werden. Dazu mit "<>" C-Style auswählen und Device EUI und Application EUI auf "lsb" einstellen. Der App Key bleibt bei "msb". Mit dem Button ganz rechts können die EUIs und der Key in die Zwischenablage kopiert werden.

![TTN1](Pictures_TTN/Screenshot_20201028_192415.png)

12. In der Firmware die drei Daten in die Datei "defines.h" kopieren.

![TTN1](Pictures_TTN/Screenshot_20201028_192624.png)

13. Mit dem "->" Pfeil Symbol wird die Firmware compiliert und auf den ESP32 geflashed.

![TTN1](Pictures_TTN/Screenshot_20201028_192835.png)

14. Wenn man auf das Stecker-Symbol klickt, werden die Debug-Ausgaben angezeigt. Der Text "Packet queued" ist ein gutes Zeichen, dass der Sensor seine Daten verschickt hat.

![TTN1](Pictures_TTN/Screenshot_20201028_193319.png)

15. Zurück im TTN sollte der Status auf Grün gewechselt haben. Die übertragenen Daten lassen sich unter dem Reiter "Data" einsehen.

![TTN1](Pictures_TTN/Screenshot_20201028_193343.png)

16. Hier solle jede Minute eine neue Zeile erscheinen. Nun wird die Datenweitergabe an das Cayenne Dashboard vorbereitet. Dazu muss auf Application->Application ID geklickt werden.

![TTN1](Pictures_TTN/Screenshot_20201028_193511.png)

17. "Payload Formats" auswählen.

![TTN1](Pictures_TTN/Screenshot_20201028_193526.png)

18. "Cayenne LPP" auswählen.

![TTN1](Pictures_TTN/Screenshot_20201028_193540.png)

19. Mit "Save" bestätigen.

![TTN1](Pictures_TTN/Screenshot_20201028_193550.png)

20. Unter Applications->Application ID->Devices->Device ID->Data sieht man nun im Payload die interpretierten Werte.

![TTN1](Pictures_TTN/Screenshot_20201028_193638.png)

21. Unter Applications->Application ID->Integrations "+ add integration" klicken.

![TTN1](Pictures_TTN/Screenshot_20201028_193652.png)

22. "myDevices" auswählen.

![TTN1](Pictures_TTN/Screenshot_20201028_193711.png)

23. Process ID vergeben, default key wählen und mit "Add integration" bestätigen.

![TTN1](Pictures_TTN/Screenshot_20201028_193855.png)

Weiter gehts unter: [Cayenne](Cayenne.md).

