---
layout: default
title: kryptographiewende.net
lastUpdate: 2025-11-08
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

- [Transport Layer Security (TLS)](https://datatracker.ietf.org/doc/html/rfc8446#section-1) generiert geheime gemeinsame Schlüssel und schafft damit Vertraulichkeit.
- TLS-Server und -Clients [authentisieren](https://datatracker.ietf.org/doc/html/rfc8446#section-4.2.3) sich mit X.509 Public-Key-Zertifikaten und schaffen damit Authentizität.
- [TLS-Cipher-Suites](https://datatracker.ietf.org/doc/html/rfc8446#section-4.1.2) verschlüsseln die Kommunikation mit symmetrischen Schlüsseln und erhalten damit effizient die Vertraulichkeit.
- TLS-Endpoints prüfen
  - Summen mit kryptographischen Hash-Funktionen und schaffen damit Integrität,
  - Message-Authentication-Codes und schaffen damit Authentizität und Integrität,
  - digitale Signaturen und schaffen damit Verbindlichkeit.

Das TLS-Protokoll realisiert damit vertrauenswürdige Kommunikation.

## Application Layer Protocols (OSI 7)

Vielfach verwendete gesicherte Anwendungsprotokolle wie HTTPS, DNS over HTTPS, DNS over TLS, QUIC, LDAPS, FTPS, SMTPS, IMAPS, POP3S und STARTTLS basieren alle auf TLS.

[Secure Shell (SSH)](https://en.wikipedia.org/wiki/Secure_Shell) basiert ebenfalls auf asymmetrischer Kryptographie.

## Kryptographische Funktionen

sind wesentliche Bestandteile der Protokolle zur vertrauenswürdigen Kommunikation.

Kryptographische Hash-Funktionen signieren Nachrichten und prüfen Integrität.

Symmetrische Kryptographie
- verschlüsselt Daten effizient und schafft Vertraulichkeit,
- authentisiert Daten mit Message-Authentication-Codes und schafft damit Authentizität und Integrität.

Asymmetrische Kryptographie
- verschlüsselt Daten
  - ohne einen geheimen gemeinsamen Schlüssel zu senden,
  - mit einem öffentlichen Schlüssel, sodass diese Daten nur mit dem passenden privaten Schlüssel wieder entschlüsselt werden können, und schafft damit Vertraulichkeit,
- signiert Daten mit einem privaten Schlüssel, sodass diese Signatur von allen anderen mit dem passenden öffentlichen Schlüssel geprüft werden kann, und schafft damit Authentizität und Verbindlichkeit,
- generiert temporäre Schlüssel, sodass selbst eine nachfolgende Veröffentlichung des privaten Schlüssels die Vertraulichkeit nicht reduziert.

## Mathematische Konstrukte

und der notwendige Aufwand zu ihrer Lösung bilden das Fundament kryptographischer Funktionen.

- RSA basiert auf Primfaktorzerlegung.
- DH und DSA basieren auf diskreten Logarithmen in ganzzahligen endlichen Körpern oder auf elliptischen Kurven.

Shor's Algorithmus löst auf einem Quantencomputer sowohl Primfaktorzerlegung als auch diskrete Logarithmen in polynomialer statt sub-exponentieller Zeit.

## Quantencomputer

sind seit Jahren kommerziell verfügbar und die Quanten-Rechenleistung stieg in dieser Periode exponentiell.

Das künftige Wachstum dieser Rechenleistung ist ungewiss, aber wenn man die Entwicklung der letzten Jahre in die Zukunft projeziert, dann erreichen wir in 10 Jahren eventuell eine Rechenleistung, die das effiziente Entschlüsseln von aktuell als sicher eingestuften Schlüsseln wie RSA-2048 und ECC-256 ermöglicht.

Der Wegfall effektiver Kryptographie führt zum Verfehlen der Schutzziele Vertraulichkeit, Authentizität, Integrität und Verbindlichkeit.

## Quantensichere Kryptographie

[Kryptographische Hash-Funktionen](hash.html) mit ausreichendem klassischen und quanten-resistenten Sicherheitsabstand wirken den Beschleunigungen der Grover- und BHT-Quantenalgorithmen entgegen.

Symmetrische Kryptographie wirkt mit größeren Schlüssellängen ebenso den Quantenalgorithmen entgegen.

## Post-Quanten-Kryptographie (PQC)

Asymmetrische Kryptographie wirkt mit größeren Schlüssellängen jedoch nicht hinreichend Shor's Algorithmus entgegen.
Quantensichere asymmetrische Kryptographie erfordert Post-Quanten-Kryptographie.

[MLKEM](https://csrc.nist.gov/pubs/fips/203/final) ist ein quantensicherer Key-Encapsulation-Mechanism (KEM) und generiert gemeinsame geheime Schlüssel.

[MLDSA](https://csrc.nist.gov/pubs/fips/204/final) ist ein quantensicherer gitterbasierter digitaler Signaturalgorithmus.

[SLHDSA](https://csrc.nist.gov/pubs/fips/205/final), [LMS](https://datatracker.ietf.org/doc/html/rfc8708) und [XMSS](https://datatracker.ietf.org/doc/html/rfc8391) sind quantensichere hashbasierte digitale Signaturalgorithmen.

## Implementierung

Post-Quanten-Algorithmen werden von Libraries wie [OpenSSL](openssl.html) und Bouncy Castle implementiert.

Die [PQC Capabilities Matrix (PQCCM)](https://pkic.org/pqccm/) des PKI Consortiums listet einige Implementierungen und deren Algorithmen auf.
