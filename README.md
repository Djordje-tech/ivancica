# Kod Dančice — Salon za masažu (Banja Luka)

Jednostranični, potpuno statički sajt (`index.html`), spreman za deploy na Vercel bez ikakve dodatne konfiguracije.

## Šta je urađeno

- Dodati SEO/Open Graph/Twitter meta tagovi i favicon za profesionalniji izgled u pretraživačima i pri dijeljenju linka.
- Provjerena i potvrđena ispravnost cjelokupnog HTML-a i JavaScript-a (bez grešaka).
- Forma za rezervaciju sada, pored lokalne potvrde, automatski priprema i SMS poruku sa svim unesenim podacima (ime, telefon, usluga, datum, poruka) na broj salona — radi bez potrebe za serverom/bazom.
- Dodat `vercel.json` sa osnovnim sigurnosnim HTTP headerima.
- Sav postojeći dizajn, animacije (Three.js zlatni prstenovi u hero sekciji), 3D tilt galerija, flip-kartice recenzija, dvojezičnost (SR/EN) i sve sekcije iz originalnog koda su u potpunosti zadržane — ništa nije uklonjeno.

## Pokretanje lokalno

```bash
npx serve .
```

zatim otvorite `http://localhost:3000`.

## Deploy na Vercel

### Opcija A — Vercel CLI
```bash
npm i -g vercel
vercel
```
Pratite uputstva (New Project → izaberite ovaj folder → Deploy). Vercel automatski prepoznaje da je u pitanju statički sajt.

### Opcija B — Vercel Dashboard (bez terminala)
1. Otpakujte ovaj folder i postavite ga na GitHub (ili prevucite folder direktno na [vercel.com/new](https://vercel.com/new) — podržava i drag&drop deploy bez git-a).
2. Framework Preset: **Other** (statički sajt, nema build koraka).
3. Kliknite **Deploy**.

Sajt će biti dostupan na `https://vas-projekat.vercel.app` za par sekundi.

## Napomena o formi

Trenutno forma nema pravi backend (nema baze/e-maila) jer je sajt čisto statički — po Vercel free planu to znači nula servera za održavanje. Ako kasnije poželite da zahtjevi stižu direktno na e-mail ili u Google Sheet, to se lako dodaje kroz Vercel Serverless Function ili servis poput Formspree/Web3Forms — javite se pa se to nadogradi.
