# Junat (PWA)

HSL-junien lähtöajat Digitransit-rajapinnasta. Asentuu Android-puhelimen aloitusnäytölle Chromen kautta, ei APK:ta eikä sivulatausta Google Playn ohi.

Huom: PWA on sovellusikoni, ei Androidin widget. Se avautuu koko ruudun lähtötauluksi.

## Julkaisu GitHub Pagesiin

1. Luo uusi repo (esim. `junat`) ja lataa siihen kaikki tämän kansion tiedostot (index.html, manifest.webmanifest, sw.js, icon-192.png, icon-512.png).
2. Repo -> Settings -> Pages -> Deploy from a branch -> `main` / root.
3. Avaa `https://<käyttäjä>.github.io/junat/` puhelimen Chromessa.
4. Chromen valikko (⋮) -> **Asenna sovellus** / **Lisää aloitusnäytölle**.
5. Avaa sovellus -> ⚙ -> syötä API-avain ja asemat (rivi: `Nimi;HSL:ID`). Tallentuu vain puhelimen selaimeen, ei repoon.

## Toiminta

- Päivittyy 30 s välein kun sovellus on auki, ja heti kun palaat siihen. ↻ päivittää käsin.
- Vihreä aika = reaaliaikatieto, valkoinen = aikataulun mukainen.
- Päivityksen jälkeen `sw.js`:n `CACHE`-versiota ei tarvitse vaihtaa: tiedostot haetaan verkosta ensin.
