---
title: Polityka prywatności — BallparkIT
permalink: /prywatnosc/
lang: pl
---

# Polityka prywatności — BallparkIT

**Wersja rozszerzenia:** 0.1.0 · **Data:** 2026-11-17

## Krótko

Rozszerzenie nie zbiera żadnych danych o użytkowniku. Nie ma kont, nie ma
analityki, nie ma identyfikatorów, nie ma reklam. Treść oglądanej oferty nie
opuszcza przeglądarki — widełki są liczone lokalnie, przez model zapakowany
razem z kodem rozszerzenia.

Rozszerzenie nie łączy się z żadnym serwerem poza pięcioma portalami, na których
działa. Jedyny rodzaj zapytania, jaki wykonuje, jest opisany niżej.

## Co rozszerzenie wysyła

### Przy przejściu między ofertami: jedno anonimowe zapytanie do portalu

Portale ogłoszeniowe to aplikacje jednostronicowe: po kliknięciu w kolejną
ofertę adres w pasku się zmienia, ale dane poprzedniej oferty zostają w
dokumencie. Żeby nie pokazać widełek policzonych dla **innej** oferty,
rozszerzenie prosi portal o aktualną wersję strony, na której użytkownik już
jest.

To zapytanie:

- idzie **wyłącznie** do tego samego portalu i pod ten sam adres, który
  użytkownik ma otwarty — żadna nowa strona nie dowiaduje się o niczym;
- jest wysyłane **bez ciasteczek** (`credentials: "omit"`), więc portal nie
  wiąże go z sesją ani z kontem użytkownika;
- nie występuje po zwykłym wejściu na ofertę z zewnątrz ani po odświeżeniu
  strony — tylko po przejściu wewnątrz portalu.

Na justjoin.it to samo zapytanie wykonywane jest już przy wejściu na ofertę,
bo ten portal nie umieszcza danych oferty w dokumencie strony.

## Czego rozszerzenie nie robi

- nie wysyła nigdzie treści oglądanej oferty, jej adresu ani nazwy pracodawcy;
- nie łączy się z żadnym serwerem autora ani z żadną usługą zewnętrzną;
- nie tworzy ani nie przechowuje żadnego identyfikatora użytkownika;
- nie korzysta z analityki, telemetrii ani narzędzi śledzących;
- nie prosi o konto, e-mail ani żadne dane osobowe;
- nie sprzedaje i nie przekazuje danych — nie ma czego przekazać;
- nie działa poza pięcioma portalami wymienionymi niżej.

## Uprawnienia i po co

Rozszerzenie nie prosi o żadne uprawnienia przeglądarki. Jedyny dostęp, jaki
deklaruje, to możliwość uruchomienia skryptu na pięciu portalach:

| Dostęp | Po co |
| --- | --- |
| pięć portali | Odczytanie ogłoszenia i doklejenie panelu z widełkami. Zakres to całe domeny, a nie ścieżki ofert, ponieważ portale nadają swoim ofertom różne adresy i wzorzec ścieżki po prostu ich nie obejmuje. Poza stroną oferty skrypt sprawdza jedną rzecz i kończy działanie. |

Obsługiwane portale: theprotocol.it, pracuj.pl, bulldogjob.pl, nofluffjobs.com,
justjoin.it.

## Co jest przechowywane na komputerze

Nic. Rozszerzenie nie zapisuje niczego w pamięci przeglądarki ani na dysku.
Wybory wpisane w panelu znikają razem z kartą.

## Skąd biorą się widełki

Z ogłoszeń, które podały stawkę, opublikowanych na polskich portalach IT.
Model i tabela zbiorcza są zapakowane w rozszerzeniu i liczą wynik na
komputerze użytkownika — żadna oferta nie jest w tym celu nigdzie wysyłana.
Tabela zawiera wyłącznie **dane zagregowane**: jak często dany portal podaje
stawkę i ile ogłoszeń stoi za daną kombinacją roli, poziomu, formy zatrudnienia
i miasta — bez jednego ogłoszenia, nazwy pracodawcy czy linku, a komórki poniżej
pięciu ogłoszeń nie są publikowane w ogóle. Widełki są **szacunkiem
statystycznym**, a nie ofertą pracodawcy ani poradą.

## Zmiany

Zmiany tej polityki będą publikowane razem z kolejnymi wersjami rozszerzenia w
Chrome Web Store.

---

# Privacy policy — BallparkIT (English)

**Extension version:** 0.1.0 · **Date:** 2026-11-17

## In short

The extension collects nothing about its users. No accounts, no analytics, no
identifiers, no ads. The content of the offer being viewed never leaves the
browser — the salary range is computed locally by a model packaged with the
extension's own code.

The extension connects to no server other than the five job boards it runs on.
The one kind of request it makes is described below.

## What the extension sends

### On navigating between offers: one anonymous request to the board

Job boards are single-page applications: clicking through to the next offer
changes the address bar while the previous offer's data stays in the document.
To avoid showing a range computed for a **different** offer, the extension asks
the board for the current version of the page the user is already on.

That request:

- goes **only** to the same board, at the same address the user has open — no
  new party learns anything;
- is sent **without cookies** (`credentials: "omit"`), so the board cannot tie
  it to the user's session or account;
- does not happen on a normal arrival at an offer or on a page reload — only
  after navigating within the board.

On justjoin.it the same request happens on arrival, because that board does not
put the offer's data in the page document.

## What the extension does not do

- send the viewed offer's content, its URL or the employer's name anywhere;
- connect to any server of the author's or to any third-party service;
- create or store any user identifier;
- use analytics, telemetry or tracking of any kind;
- ask for an account, an email address or any personal data;
- sell or share data — there is none to share;
- run anywhere other than the five boards listed below.

## Permissions, and what each is for

The extension requests no browser permissions. The only access it declares is
the ability to run its script on five job boards:

| Access | What for |
| --- | --- |
| five boards | Reading the posting and mounting the panel. The scope is whole domains rather than offer paths because the boards give their own offers several URL shapes and a path pattern does not cover them. Away from an offer page the script checks one thing and stops. |

Supported boards: theprotocol.it, pracuj.pl, bulldogjob.pl, nofluffjobs.com,
justjoin.it.

## What is stored on the machine

Nothing. The extension writes nothing to browser storage or to disk. Choices
entered in the panel are gone when the tab is.

## Where the figures come from

From postings that stated a salary, published on Polish IT job boards. The
model and an aggregate table ship inside the extension and run on the user's
own machine — no offer is sent anywhere to be scored. The table holds
**aggregate figures only**: how often a given board states a salary, and how
many postings sit behind a combination of role, seniority, contract basis and
city — no posting, no employer name and no link, and cells built on fewer than
five postings are not published at all. The range is a **statistical
estimate**, not an employer's offer and not advice.

## Changes

Changes to this policy are published with subsequent versions of the extension
in the Chrome Web Store.
