---
layout: page
title: Zadanie
---

## Základný cieľ a architektúra
- Systém tvoria dve časti: **mobilná aplikácia (Android)** na snímanie ISIC kariet a **webová aplikácia** s hlavnou logikou.
- **Mobilná aplikácia** zaznamená príchod študenta cez NFC (vrátane časovej pečiatky príchodu) a odošle údaje na server.
- **Webová aplikácia** spravuje rozvrh, dochádzku, výučbu a integráciu s AIS.
- Aplikácia je určená **iba učiteľom**, študenti do nej prístup nemajú.

## Priebeh evidencie na hodine
- Telefón leží na stole učiteľa pri katedre.
- Študent pri príchode priloží ISIC kartu k zadnej strane telefónu.
- Aplikácia dá okamžitú spätnú väzbu: **zelená obrazovka a zvuk** pri úspechu, **červená obrazovka a chybový zvuk** pri neúspechu (predvolená hlasitosť je nízka).

## Správa semestra a rozvrhu
- Nastavenie začiatku a konca semestra (počet týždňov sa vypočíta automaticky), dní voľna a presunov výučby (napr. výučba v utorok podľa rozvrhu zo stredy).
- Synchronizácia s **Google Kalendárom** školy pre voľné dni a presuny (admin ju nastaví globálne na začiatku semestra).
- Predmety s typmi (prednáška, seminár, cvičenie, laboratórne cvičenie), miestnosťou, časom a opakovaním (týždenne alebo každý druhý týždeň).
- Podpora **paralelných skupín** (skupiny A a B v rovnakom dni a čase).

## Dáta a prepojenie s AIS
- Import študentov z AIS cez exportované **CSV** súbory pre konkrétne cvičenia.
- Ak má cvičiaci dve skupiny v rovnakom čase, študenti sa exportujú spolu (oddelení prázdnym riadkom). Ak majú dvaja cvičiaci cvičenie v rovnakom čase, každý rieši svoje.
- **Statusy dochádzky:** prítomný, neprítomný, ospravedlnený, nahrádza. Predvolený stav je neprítomný, s možnosťou ručnej úpravy.
- **Náhrady:** pri statuse „nahrádza“ systém eviduje prepojenie s druhým cvičením. Na cvičení, kde študent nahrádza, je vizuálne odlíšený (pod čiarou, na konci prehľadu) so statusom prítomný. Na pôvodnom cvičení má status „nahrádza“.
- **Prehľad a export:** matica dochádzky (riadky = študenti, stĺpce = týždne, bunka = skratka stavu), export kompletnej dochádzky a štatistika ospravedlnených a neospravedlnených neprítomností.

## Úlohy podľa zadania
1. Nájsť a zvoliť vhodné knižnice na snímanie ISIC kariet v Androide.
2. Navrhnúť vhodnú architektúru systému.
3. Implementovať systém (mobilnú aj webovú časť).
4. Verifikovať a otestovať funkčnosť systému.
