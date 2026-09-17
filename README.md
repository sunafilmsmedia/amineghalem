# Site — El-Amine Ghalem (courtier immobilier)

Page unique, self-contained (`index.html`). Aucune dépendance, aucun build.
Hébergement statique recommandé : Vercel ou Netlify.

## À faire avant mise en ligne (voir brief)

**Placeholders**
- Téléphone / courriel : `514 000-0000` et `info@example.com` (dans `index.html` **et** dans le JSON-LD du `<head>`).
- Photo À propos : bloc « Photo d'El-Amine » → `<img>` WebP, max 800 px, `alt="El-Amine Ghalem, courtier immobilier"`.
- Propriétés : fonds dégradés → photos WebP, max 900 px, `loading="lazy"`.
- Nom exact de l'agence : `RE/MAX` (footer + JSON-LD).
- `favicon` + `og:image` (1200×630).

**Formulaire → GoHighLevel**
- Dans le `<script>` : `const WEBHOOK_URL = ""` → coller l'URL de l'Inbound Webhook GHL.
- Payload JSON : `prenom, nom, tel, email, adresse, projet` + `tag: site-evaluation`.

**Tracking** (dans le `<head>`, emplacements commentés)
- Meta Pixel — l'événement `Lead` est déjà câblé dans le handler du formulaire.
- GA4 / GTM.

**SEO / IA** (fichiers déjà présents à la racine)
- `robots.txt`, `sitemap.xml`, `llms.txt` — remplacer le domaine si différent de `elamineghalem.com`.
- Tester le JSON-LD : search.google.com/test/rich-results.
- Google Search Console + fiche Google Business.

## Déploiement rapide
- Vercel : `vercel --prod` (ou import du repo), aucun réglage de build.
- Netlify : glisser-déposer le dossier, ou connecter le repo.
- Forcer HTTPS + redirection `www` → non-`www`.
