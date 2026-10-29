# Finansų harmonija V19

Užfiksuota testavimo versija, žyma `v19`. Tolesni pakeitimai atliekami tik atskirame V20 projekte. V19 ir ankstesni leidimai nekeičiami.

Testavimo adresas: https://albertborkovski-cmd.github.io/finansu-harmonija-v19/

Šioje saugykloje yra paruoštas statinis V19 testavimo leidimas. Tikslus išeities kodas pateiktas faile [source-v19.zip](./source-v19.zip), iš vietinio Git įrašo `3ad31c4b14409d9f99d0ecc9192a735af7abf4bb`. Archyve nėra vietinių duomenų, slaptažodžių ar `node_modules`.

## Vietinis paleidimas iš source-v19.zip

```bash
npm ci
npm run dev
```

Vietinis V19 adresas: http://127.0.0.1:5200/.
Aktyvaus V20 adresas: http://127.0.0.1:5201/.

## Testavimo prisijungimas

- Vidinio administratoriaus demonstracija: `albertborkvski@gmail.com`.
- Išorinio naudotojo demonstracija: `aurika.z@meso.lt`.
- Slaptažodžio laukas šiame prototipe tikrina tik formatą: bent 6 simboliai, didžioji raidė ir specialus simbolis. Naudokite išgalvotą testinę reikšmę, ne tikrą slaptažodį.

Tai demonstracinis prototipas, ne produkcinė apskaitos sistema. GitHub Pages versijoje nėra saugaus serverinio autentifikavimo, bendros duomenų bazės, tikro OCR vykdymo ar laiškų siuntimo serverio. Demonstraciniai vaidmenys nėra saugumo riba. Nenaudokite konfidencialių dokumentų ar tikrų slaptažodžių.

Vietiniai `.env`, `.meso-shared-data.json`, `node_modules` ir darbo katalogų failai nepublikuojami. Interneto versija naudoja demonstracinius ir naršyklėje saugomus duomenis. To paties GitHub Pages domeno senesni leidimai gali dalytis naršyklės saugykla; izoliuotam testavimui naudokite atskirą naršyklės profilį.

## Leidimo patikra

- `npm run typecheck` ir `npm run build` praeina.
- Pilnas esamų testų paleidimas: 669 praėjo, 10 nepraėjo. Nepraėję senesni UI testai turi `import.meta` / CommonJS bei `useWorkspaceExpansion` testinių priklausomybių neatitikimų. Jų taisymas paliekamas V20; šis leidimas išsaugo dabartinę naudotojo testuojamą programos versiją.
- Atskiros viešos nuorodos, kurioms reikalingi serverio maršrutai, statiniame GitHub Pages prototipe gali neveikti.
