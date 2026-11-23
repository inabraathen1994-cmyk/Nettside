# Ina Haugane Braathen – nettside

Dette er nettsiden din. Du eier den selv, og du trenger ikke jobbkontoen eller Claude for å bruke eller oppdatere den.

**Slik henger det sammen:**
- **GitHub** lagrer filene og viser siden på nett. Det er gratis.
- **Pages CMS** er et redigeringsverktøy i nettleseren. Der laster du opp arbeider og endrer tekst, uten å røre kode.
- **Domeneshop** (eller en annen registrar) selger domenet, for eksempel `inabraathen.no`. Det koster ca. 100–200 kr i året.

Bruk **privat e-post** på alle kontoene, ikke jobb-e-posten.

---

## 0. Ta med deg mappa

Mappa `Ina-nettside` ligger på jobbmaskinen. Kopier den til et sted du har tilgang til etter at du slutter, for eksempel en minnepenn eller din private iCloud eller Google Drive. Den er også lagret som `Ina-nettside.zip` på skrivebordet. Når steg 2 er gjort, ligger alt trygt på GitHub.

## 1. Lag en GitHub-konto

Gå til github.com og trykk **Sign up**. Brukernavnet blir en del av den midlertidige adressen, for eksempel `inabraathen.github.io`.

## 2. Last opp nettsiden

1. Trykk **+** øverst til høyre og velg **New repository**.
2. Kall det `nettside`, velg **Public** og trykk **Create repository**.
3. Trykk **uploading an existing file**.
4. Dra inn **innholdet** i mappa `Ina-nettside`: `index.html`, `README.md` og mappene `content` og `media`. Ikke dra inn selve mappa.
   - Fila `.pages.yml` er skjult i Finder. Trykk **Cmd + Shift + .** (punktum) i Finder for å vise den, og dra den med.
5. Trykk **Commit changes**.

## 3. Slå på nettsiden

1. Åpne repoet og gå til **Settings**, deretter **Pages**.
2. Under **Branch** velger du `main` og `/ (root)`, og trykker **Save**.
3. Etter 1–2 minutter ligger siden på `https://BRUKERNAVN.github.io/nettside/`.

## 4. Kjøp domenet og koble det til

1. Kjøp `inabraathen.no` hos domeneshop.no. Det var ledig per 23. november 2026. Et .no-domene krever norsk fødselsnummer.
2. Åpne DNS-innstillingene for domenet hos Domeneshop og legg inn disse fire **A-postene** for selve domenet (feltet for navn står tomt):
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
3. Legg inn én **CNAME-post**: navn `www`, peker til `BRUKERNAVN.github.io`.
4. Gå tilbake til GitHub, åpne **Settings** og så **Pages**. Skriv `inabraathen.no` under **Custom domain** og trykk **Save**.
5. Når sjekken er grønn, huker du av **Enforce HTTPS**. Det kan ta fra noen minutter til et døgn før domenet virker.

## 5. Legg til og endre arbeider

1. Gå til **app.pagescms.org** og velg **Sign in with GitHub**.
2. Gi tilgang til repoet `nettside` når du blir spurt (det heter «Install the GitHub App»).
3. Åpne repoet og velg **Nettside** i menyen.
4. Under **Arbeider** trykker du **Add**. Fyll inn tittel, kategori og år, og last opp bilder, video eller PDF.
   - Det første bildet blir forsidebildet.
   - Det arbeidet som ligger øverst i lista, vises først på siden. Du kan dra for å endre rekkefølgen.
5. Trykk **Save**. Etter omtrent ett minutt er endringen synlig på siden.

På samme sted endrer du LinkedIn- og Behance-lenkene og «Om meg»-teksten.

**Tips til filer:**
- **Bilder:** Eksporter i rundt 2000 px på den lengste siden, og som JPG eller WebP under 1–2 MB. Da laster siden raskt.
- **Video:** Hold den kort og under 25 MB. Lengre filmer legger du på Vimeo, YouTube eller Behance, og lenker til dem i feltet «Lenke til prosjektet».
- **PDF:** Vises som en «Åpne PDF»-knapp.

Første gang du lagrer et arbeid: sjekk at bildet faktisk vises på siden. Hvis det ikke gjør det, er det noe med oppsettet. Spør Claude (se under).

## 6. Større endringer med Claude

Hele nettsiden ligger i **én fil: `index.html`**. Den inneholder design, farger, animasjoner, CV og portrett. Du kan dobbeltklikke på den for å se siden i nettleseren, også uten internett (da mangler bare skrifttypene).

1. Lag en gratis Claude-konto på claude.ai med privat e-post.
2. Start en ny samtale, last opp `index.html` og skriv hva du vil endre. For eksempel: «Legg til en ny jobb i CV-en», «gjør overskriftene større» eller «bytt den rosa fargen til lys blå». Øverst i fila står en forklaring som Claude leser, så du trenger ikke forklare oppbygningen.
3. Be om å få hele fila tilbake. Lagre den som `index.html`.
4. Last den opp i GitHub-repoet med **Add file** og så **Upload files**. Samme filnavn erstatter den gamle.

Hvem bestemmer hva:
- **I Pages CMS:** arbeider, lenker, «Om meg», farger og portrett. Når siden ligger på nett, vinner det du har lagret i Pages CMS over det som står i `index.html`.
- **I `index.html`, via Claude:** CV, navn, e-post, design, oppsett og animasjoner.

Vil du heller la Claude endre arbeider eller lenker, laster du også opp `content/site.json` og ber Claude endre den.

## Filene

| Fil | Hva den er |
|---|---|
| `index.html` | Hele nettsiden: design, animasjoner, CV, portrett og kode |
| `content/site.json` | Arbeider, lenker, om-tekst, farger og portrett. Redigeres i Pages CMS |
| `media/` | Bilder, video og PDF du laster opp i Pages CMS |
| `.pages.yml` | Oppsettet for Pages CMS (skjult fil) |
| `README.md` | Denne guiden |
