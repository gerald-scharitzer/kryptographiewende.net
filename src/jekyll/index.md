---
layout: default
title: Home
lastUpdate: 2025-10-18
---
# Die Kryptographiewende

bringt den Wandel der grundlegenden Algorithmen vertrauensbasierter Systeme.

Unsere Informationsgesellschaft basiert auf den Funktionen der Kryptographie zum Erhalt der folgenden [Eigenschaften](https://de.wikipedia.org/wiki/Informationssicherheit#Motivation_und_Ziele_der_Informationssicherheit).

- __Vertraulichkeit__: Wir kommunizieren miteinander und nur wir wissen, was wir einander gesendet haben.
- __Authentizität__: Wir wissen, mit wem wir kommunizieren.
- __Integrität__: Was wir empfangen haben ist, was uns gesendet wurde.
- __Verbindlichkeit__: Wir wissen, wer was gesendet hat.

Diese Eigenschaften der Kommunikation machen sie vertrauenswürdig.

## Transport Layer Security (TLS)

Wesentliche Fähigkeiten unserer Gesellschaft basieren auf effizienter vertrauenswürdiger Kommunikation.

- [Transport Layer Security (TLS)](https://datatracker.ietf.org/doc/html/rfc8446#section-1) generiert einen geheimen gemeinsamen Schlüssel und schafft damit Vertraulichkeit.
- TLS-Server und -Clients [authentisieren](https://datatracker.ietf.org/doc/html/rfc8446#section-4.2.3) sich mit X.509 Public-Key-Zertifikaten und schaffen damit Authentizität.
- [TLS-Cipher-Suites](https://datatracker.ietf.org/doc/html/rfc8446#section-4.1.2) kommunizieren verschlüsselt mit symmetrischen Schlüsseln und erhalten damit effizient die Vertraulichkeit.
- TLS-Endpoints prüfen
  - Summen mit kryptographischen Hash-Funktionen und schaffen damit Integrität
  - Message-Authentication-Codes und schaffen damit Authentizität und Integrität
  - digitale Signaturen und schaffen damit Verbindlichkeit.

## Application Layer Protocols (OSI 7)

Vielfach verwendete gesicherte Anwendungsprotokolle wie HTTPS, DNS over HTTPS, DNS over TLS, QUIC, LDAPS, FTPS, SMTPS, IMAPS, POP3S und STARTTLS basieren alle auf TLS.

[Secure Shell (SSH)](https://en.wikipedia.org/wiki/Secure_Shell) basiert ebenfalls auf asymmetrischer Kryptographie.

## Kryptographische Funktionen

Diese Eigenschaften und Protokolle beruhen auf kryptographischen Funktionen.

Kryptographische Hash-Funktionen signieren Nachrichten und prüfen Integrität.

Symmetrische Kryptographie
- verschlüsselt Daten effizient und schafft Vertraulichkeit,
- authentisiert Daten mit Message-Authentication-Codes und schafft damit Authentizität und Integrität.

Asymmetrische Kryptographie
- verschlüsselt Daten, ohne einen geheimen gemeinsamen Schlüssel zu senden,
- verschlüsselt Daten mit einem öffentlichen Schlüssel, sodass diese Daten nur mit dem passenden privaten Schlüssel wieder entschlüsselt werden können, und schafft damit Vertraulichkeit,
- signiert Daten mit einem privaten Schlüssel, sodass diese Signatur von allen anderen mit dem passenden öffentlichen Schlüssel geprüft werden kann, und schafft damit Authentizität und Verbindlichkeit,
- generiert temporäre Schlüssel, sodass selbst eine nachfolgende Veröffentlichung des privaten Schlüssels die Vertraulichkeit nicht reduziert.

## Mathematische Konstrukte

und der notwendige Aufwand zu ihrer Lösung bilden das Fundament kryptographischer Funktionen.

- RSA basiert auf Primfaktorzerlegung.
- DH und DSA basieren auf diskreten Logarithmen in ganzzahligen endlichen Körpern oder auf elliptischen Kurven.

Shor's Algorithmus löst auf einem Quantencomputer sowohl Primfaktorzerlegung als auch diskrete Logarithmen in polynomialer Zeit.
