---
layout: default
title: Kryptographiewende
lastUpdate: 2025-10-16
---
# Die Kryptographiewende

bringt den Wandel der grundlegenden Algorithmen vertrauensbasierter Systeme.

Unsere Informationsgesellschaft basiert auf den Funktionen der Kryptographie zum Erhalt der folgenden [Eigenschaften](https://de.wikipedia.org/wiki/Informationssicherheit#Motivation_und_Ziele_der_Informationssicherheit).

- __Vertraulichkeit__: Wir kommunizieren miteinander und nur wir wissen, was wir miteinander kommuniziert haben.
- __Authentizität__: Wir wissen, mit wem wir kommunizieren.
- __Integrität__: Was wir empfangen haben ist, was uns gesendet wurde.
- __Verbindlichkeit__: Wir wissen, wer was kommuniziert hat.

Diese Eigenschaften der Kommunikation machen sie vertrauenswürdig.

## Transport Layer Security (TLS)

Wesentliche Fähigkeiten unserer Gesellschaft basieren auf effizienter vertrauenswürdiger Kommunikation.

- [Transport Layer Security (TLS)](https://datatracker.ietf.org/doc/html/rfc8446#section-1) generiert einen geheimen gemeinsamen Schlüssel und schafft damit Vertraulichkeit.
- TLS-Server und -Clients [authentisieren](https://datatracker.ietf.org/doc/html/rfc8446#section-4.2.3) sich mit X.509 Public-Key-Zertifikaten und schaffen damit Authentizität.
- [TLS-Cipher-Suites](https://datatracker.ietf.org/doc/html/rfc8446#section-4.1.2) kommunizieren verschlüsselt mit symmetrischen Schlüsseln und erhalten damit effizient die Vertraulichkeit.
- TLS-Endpoints prüfen mit kryptographischen Hash-Funktionen und schaffen damit Integrität.
- TLS-Endpoints prüfen Message-Authentication-Codes und schaffen damit Authentizität und Integrität.

## Application Layer Protocols (OSI 7)

HTTPS, DNS over HTTPS, DNS over TLS, and STARTTLS all use TLS.

[Secure Shell (SSH)](https://en.wikipedia.org/wiki/Secure_Shell) basiert ebenfalls auf public key cryptography und key exchange.

## Kryptographische Funktionen

Diese beruhen auf kryptographischen Funktionen.

Kryptographische Hash-Funktionen signieren Nachrichten und prüfen Integrität.

Symmetrische Kryptographie
- verschlüsselt Daten effizient und schafft Vertraulichkeit,
- authentisiert Daten mit Message-Authentication-Codes und schafft damit Authentizität und Integrität.

Asymmetrische Kryptographie
- verschlüsselt Daten, ohne einen geheimen gemeinsamen Schlüssel zu senden,
- verschlüsselt Daten mit einem öffentlichen Schlüssel, sodass diese Daten nur mit dem passenden privaten Schlüssel wieder entschlüsselt werden können, und schafft damit Vertraulichkeit,
- signiert Daten mit einem privaten Schlüssel, sodass diese Signatur von allen anderen mit dem passenden öffentlichen Schlüssel geprüft werden kann, und schafft damit Authentizität und Verbindlichkeit,
- generiert temporäre Schlüssel, sodass selbst eine nachfolgende Veröffentlichung des privaten Schlüssels die Vertraulichkeit nicht reduziert.
