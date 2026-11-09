# AnalizaFin Pro – actualizări

Adresa folosită de program: `Maryanbmd/analizafin-actualizari` (fișierele se citesc de la https://raw.githubusercontent.com/Maryanbmd/analizafin-actualizari/main/).

Acest depozit ține la zi programul **AnalizaFin Pro** instalat pe calculatoare.

| Fișier | Rol |
|---|---|
| `reguli.json` | Regulile fiscale: cote (TVA, profit, dividende, micro, CAS, CASS, CAM), plafoane, termene, zile libere și **anunțuri legislative** |
| `versiune.json` | Ultima versiune a programului: număr, noutăți și amprenta SHA-256 a fișierului |
| `app/index.html` | Programul propriu-zis (se descarcă la actualizare și se verifică după amprenta SHA-256) |

## Cum se actualizează regulile
1. Deschide `reguli.json` → creionul ✏️ (Edit).
2. Modifică valoarea (ex. `"tva_red": 11`) și **mărește `versiune`** (ex. `2026.12.15`).
3. Opțional, adaugă un anunț în `anunturi` (cu `id` unic, `data`, `titlu`, `text`, `link`).
4. *Commit changes*. Programele vor afișa modificarea la următoarea verificare.

## Cum se publică o versiune nouă a programului
1. Încarcă noul `app/index.html` (Add file → Upload files, în folderul `app`).
2. În `versiune.json` modifică `versiune`, `data`, `noutati` și `sha256` (amprenta noului fișier).

Depozitul trebuie să fie **Public** pentru ca programul să poată citi fișierele fără autentificare.
