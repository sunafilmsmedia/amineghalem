# Site — El-Amine Ghalem (courtier immobilier RE/MAX Alliance)

Page unique, self-contained (`index.html`). Charte RE/MAX (rouge `#DC1C2E` / bleu `#003DA5` / blanc).
Aucun build. Hébergement statique : Vercel ou Netlify.

## Fichiers
- `index.html` — le site
- `amine.jpg` — portrait d'El-Amine (section À propos, 461×564)
- `amine-banner.jpg` — bannière lifestyle (utilisée en og:image de partage, 2000×1000)
- `remax-alliance.svg` — logo RE/MAX Alliance (footer)
- `robots.txt`, `sitemap.xml`, `llms.txt` — SEO / IA (remplacer le domaine si ≠ elamineghalem.com)

## À faire avant mise en ligne

**Placeholders texte**
- Téléphone / courriel : `514 000-0000` et `info@example.com` (dans `index.html` **et** dans le JSON-LD du `<head>`).
- `favicon` + `og:image` (1200×630).

**Vidéo de fond du hero → Wistia** ✅ en place
- IDs branchés : `twot4oqwkq` puis `qm71omu8oz` (dans `var HERO_WISTIA` en bas de `index.html`).
- Les 2 clips s'enchaînent en boucle, sans coupure, en muet + autoplay + cover.

**Formulaire → GoHighLevel**
- Dans le `<script>` : `const WEBHOOK_URL = ""` → coller l'URL de l'Inbound Webhook GHL.
- Payload JSON : `prenom, nom, tel, email, adresse, projet` + `tag: site-evaluation`.

**Tracking** (dans le `<head>`, emplacements commentés)
- Meta Pixel — l'événement `Lead` est déjà câblé dans le handler du formulaire.
- GA4 / GTM.

**SEO / IA**
- Tester le JSON-LD : search.google.com/test/rich-results.
- Google Search Console + fiche Google Business.

## Déploiement rapide
- Vercel : import du repo, aucun réglage de build.
- Netlify : glisser-déposer le dossier, ou connecter le repo.
- Forcer HTTPS + redirection `www` → non-`www`.

## Notes perf
- La vidéo Wistia charge le script `E-v1.js` (externe) → surveiller le PageSpeed mobile (objectif ≥ 90).
- Portrait `amine.jpg` : 461 px de large. Correct, mais une version ≈ 800 px (< 200 Ko) serait plus nette sur grand écran.
