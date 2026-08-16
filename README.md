# Atelierul Tudosie

Site-ul atelierului: mobilier din lemn masiv, la comandă, din 2002.

## Ce este aici

Un singur fișier `index.html` și un folder `assets/`. Fără framework, fără pas de build,
fără cod de server. Exact fișierele acestea ajung pe internet, așa cum sunt.

```
index.html          toată pagina: structură, stiluri, animații
assets/
  hero-scrub.mp4    filmul de sus, derulat de scroll
  hero-poster.jpg   primul cadru, afișat cât se încarcă filmul
  hero-ending.jpg   cadrul final, folosit pe telefon și la finalul paginii
  *.jpg             fotografiile pieselor
```

## Cum se vede local

Filmul are nevoie de un server local, pentru că browserul blochează încărcarea
fișierelor mari direct de pe disc. Din acest folder:

```
npx http-server -p 8899 -c-1
```

Apoi deschideți `http://localhost:8899` în browser.

Dacă deschideți `index.html` cu dublu clic, pagina funcționează, dar în locul filmului
apare imaginea fixă. Asta este comportamentul proiectat, nu o defecțiune.

## Cum se modifică datele de contact

Numărul de telefon, WhatsApp și adresa de email apar în `index.html`, marcate cu
comentariul `<!-- CONTACT -->`. Se schimbă în toate locurile marcate.

## Cum se publică o modificare

Orice schimbare salvată și trimisă pe GitHub ajunge automat pe site în câteva secunde:

```
git add -A
git commit -m "descrierea schimbării"
git push
```
