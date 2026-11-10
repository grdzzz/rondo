# Rondo

Web de lloguer de material de muntanya, neu i aigua per hores. És una web estàtica (HTML, CSS i JavaScript), sense servidor ni dependències.

## Fitxers

| Fitxer | Què és |
|---|---|
| `index.html` | Portada |
| `botiga.html` | Catàleg, reserva per dia i hora, cistella i confirmació |
| `rondo.css` | Colors, tipografies, capçalera, peu i botons compartits |
| `brand/` | Logo (banyes) en vermell i en clar |

## Publicar-la amb GitHub Pages

1. Crea un repositori nou a GitHub i puja-hi tots els fitxers d'aquesta carpeta.
2. Ves a **Settings → Pages**.
3. A **Source**, tria **Deploy from a branch**, branca `main` i carpeta `/ (root)`. Desa.
4. Al cap d'un minut la web és a `https://<el-teu-usuari>.github.io/<nom-del-repo>/`.

## Què cal canviar abans d'obrir-la al públic

- **Productes i preus:** la llista `PRODUCTS` al principi del `<script>` de `botiga.html`.
- **Horari:** `OPEN` i `CLOSE` a `botiga.html`. Si el canvieu, actualitzeu també el text del peu i de la portada.
- **Fotos:** ara són d'Unsplash (llicència lliure). Substituïu-les per fotos pròpies: camp `img` de cada producte a `botiga.html` i etiquetes `<img>` a `index.html`.
- **Tipografia:** el brandboard fa servir Nexa, que no és a Google Fonts. Ara es fa servir Outfit. Amb la llicència de Nexa, canvieu `--font-head` a `rondo.css`.

## Limitacions

- **La disponibilitat és simulada.** La funció `externalBusy()` de `botiga.html` inventa l'ocupació d'altres clients.
- **Les reserves es guarden només al navegador de qui reserva** (`localStorage`). No arriben a la botiga.

Per rebre reserves de veritat cal un servidor o una base de dades (per exemple Supabase o Firebase).
