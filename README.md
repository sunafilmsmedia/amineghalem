# Site — El-Amine Ghalem (courtier immobilier RE/MAX Alliance)

Page unique, self-contained (`index.html`). Charte RE/MAX (rouge `#DC1C2E` / bleu `#003DA5` / blanc).
Aucun build. Hébergement statique : Vercel ou Netlify.

## Fichiers
- `index.html` — le site
- `amine.avif` — photo d'El-Amine (section À propos)
- `remax-alliance.svg` — logo RE/MAX Alliance (footer)
- `robots.txt`, `sitemap.xml`, `llms.txt` — SEO / IA (remplacer le domaine si ≠ elamineghalem.com)

## À faire avant mise en ligne

**Placeholders texte**
- Téléphone / courriel : `514 000-0000` et `info@example.com` (dans `index.html` **et** dans le JSON-LD du `<head>`).
- `favicon` + `og:image` (1200×630).

**Vidéo de fond du hero → Wistia**
- Hébergée sur Wistia. Dans le `<script>` en bas : `var HERO_WISTIA = ['VIDEO_ID_1','VIDEO_ID_2']`.
- Remplacer par les 2 hashed IDs (Wistia → média → Embed & Share → Inline Embed → les 10 caractères après `wistia_async_`).
- Les 2 clips s'enchaînent en boucle, sans coupure, en muet + autoplay. Tant que les IDs ne sont pas mis, le fond reste bleu uni.

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
- Photo `amine.avif` : actuellement 320×400 px. Fournir une version plus haute résolution (≈ 800 px de large, < 200 Ko) pour un rendu net sur desktop.
