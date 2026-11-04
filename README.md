# ⚽ Fotbollsträning – planerare

En enkel webbapp för att planera träningspass för ett fotbollslag (7–8 år).
Allt ligger i `index.html` – ingen server, ingen databas, inga beroenden.

## Funktioner

- **Övningsbank** med alla övningar, filtrerbar per kategori och sökbar.
- **Veckans pass**: välj veckodag (mån–sön) och bygg ett pass av övningar.
- Tid per övning (förvald, kan justeras med − / +) och **total tid** för passet.
- Fördelning per kategori (stapel) så du ser balansen i passet.
- Ändra ordning och ta bort övningar.
- **Markera genomfört** per pass, och "Ny vecka" för att nollställa markeringarna.
- Sparas i `localStorage` – alltså bara på den enhet du använder.

## Lägga till övningar

Öppna `index.html` och leta upp `const exercises = [`. Kopiera ett block:

```js
{ id:"min-ovning", category:"boll", name:"Min övning", minutes:8,
  desc:"Hur övningen går till.",
  tip:"Ett coachtips.", gear:"Koner, bollar" },
```

- `id` måste vara unikt och ska inte ändras senare (sparade pass pekar på det).
- `category` är en av nycklarna i `categories` (uppvarmning, boll, passning,
  skott, fys, styrka, spel, avslutning). Nya kategorier läggs till där.

## Publicera på GitHub Pages

1. Settings → Pages → Deploy from branch → `main` / root.
2. Öppna sidan i mobilen (https://thompaaa.github.io/fotbollstraning/) och välj "Lägg till på hemskärmen".

Förhandsgranska lokalt:

```
python3 -m http.server 8000
```
