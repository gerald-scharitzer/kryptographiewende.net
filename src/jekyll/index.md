---
layout: default
title: Kryptographiewende
lastUpdate: 2025-10-12
---
# Die Kryptographiewende

bringt den Wandel der grundlegenden Algorithmen vertrauensbasierter Systeme.

Unsere Informationsgesellschaft basiert auf den Funktionen der Kryptographie zum Erhalt der folgenden [Eigenschaften](https://de.wikipedia.org/wiki/Informationssicherheit#Motivation_und_Ziele_der_Informationssicherheit).

- __Vertraulichkeit__: Wir kommunizieren miteinander und nur wir wissen, was wir miteinander kommuniziert haben.
- __Authentizität__: Wir wissen, mit wem wir kommunizieren.
- __Integrität__: Was wir empfangen haben ist, was uns gesendet wurde.
- __Verbindlichkeit__: Wir wissen, wer was kommuniziert hat.

Diese Eigenschaften der Kommunikation machen sie vertrauenswürdig.

Wesentliche Fähigkeiten unserer Gesellschaft basieren auf effizienter vertrauenswürdiger Kommunikation.

- [Transport Layer Security (TLS)](https://datatracker.ietf.org/doc/html/rfc8446#section-1) generiert einen geheimen gemeinsamen Schlüssel und schafft damit Vertraulichkeit.
- TLS-Server und -Clients authentisieren sich mit X.509 Public-Key-Zertifikaten und schaffen damit Authentizität.
- [TLS-Cipher-Suites](https://datatracker.ietf.org/doc/html/rfc8446#section-4.1.2) kommunizieren verschlüsselt mit symmetrischen Schlüsseln und erhalten damit effizient die Vertraulichkeit.
- TLS-Endpoints prüfen mit kryptographischen Hash-Funktionen und schaffen damit Integrität.
- TLS-Endpoints prüfen Message-Authentication-Codes und schaffen damit Verbindlichkeit.
