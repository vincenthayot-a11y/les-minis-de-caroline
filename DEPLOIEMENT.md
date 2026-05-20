# 🚀 Guide de mise en ligne sur GitHub Pages

Ce guide t'explique en 10 minutes comment publier le site **Les Minis de Caroline** sur GitHub Pages, gratuitement, en HTTPS.

URL finale du site : **https://vincenthayot-a11y.github.io/les-minis-de-caroline/**

---

## 📦 Contenu du pack

Tu as **7 fichiers** à uploader sur GitHub :

| Fichier | Rôle |
|---|---|
| `index.html` | Le site complet (avec toutes les images en base64) |
| `og-image.jpg` | Image d'aperçu pour les partages sur WhatsApp/Facebook/Insta |
| `robots.txt` | Autorise les moteurs de recherche à indexer le site |
| `sitemap.xml` | Aide Google à trouver et indexer les pages |
| `.nojekyll` | Fichier vide qui désactive Jekyll (par sécurité) |
| `README.md` | Description du projet sur la page GitHub du repo |
| `DEPLOIEMENT.md` | Ce guide (pour référence ultérieure) |

---

## ÉTAPE 1 — Finaliser la création du repository

Tu es déjà sur la page de création avec :
- **Owner** : `vincenthayot-a11y`
- **Repository name** : `les-minis-de-caroline`

Avant de valider, vérifie / configure :

1. **Description** *(optionnel mais utile)* : `Site officiel de l'association Les Minis de Caroline`
2. **Visibility** : ✅ **Public** *(obligatoire pour GitHub Pages gratuit)*
3. ❌ **Ne coche PAS** « Add a README file »
4. ❌ **Ne coche PAS** « Add .gitignore »
5. ❌ **Ne coche PAS** « Choose a license »

*(Tu vas uploader le README depuis le pack — si tu en crées un ici, il y aura un conflit.)*

6. Clique **« Create repository »** en bas de la page

---

## ÉTAPE 2 — Uploader les fichiers

Sur la page du repo qui vient d'être créé :

1. Tu vois la page « Quick setup ». Clique sur le lien bleu **« uploading an existing file »**
2. Une zone de drag-and-drop apparaît
3. **Glisse-dépose les 7 fichiers** du pack en même temps :
   - `index.html`
   - `og-image.jpg`
   - `robots.txt`
   - `sitemap.xml`
   - `.nojekyll`
   - `README.md`
   - `DEPLOIEMENT.md`
4. En bas de la page, dans **« Commit changes »** :
   - Laisse le message par défaut, ou écris : `Initial site upload`
   - Garde la sélection sur **« Commit directly to the main branch »**
5. Clique sur le bouton vert **« Commit changes »**

⚠️ **Le fichier `.nojekyll` est crucial**. Comme il commence par un point, il peut être invisible dans le Finder (Mac) ou l'Explorateur (Windows).
- **Sur Mac** : dans le Finder, fais `Cmd+Shift+.` pour afficher les fichiers cachés
- **Sur Windows** : dans l'Explorateur, va dans Affichage → coche « Éléments masqués »

Sans ce fichier, certains chemins de ton site peuvent ne pas fonctionner sur GitHub Pages.

---

## ÉTAPE 3 — Activer GitHub Pages

1. Sur la page du repo, va dans l'onglet **« Settings »** (tout en haut, à droite)
2. Dans le menu de gauche, clique sur **« Pages »**
3. Dans la section **« Build and deployment »** :
   - **Source** : sélectionne `Deploy from a branch`
   - **Branch** : sélectionne `main` et garde `/ (root)`
4. Clique sur **« Save »**

GitHub te dira en haut de la page (peut prendre quelques secondes à apparaître) :
> *Your site is live at https://vincenthayot-a11y.github.io/les-minis-de-caroline/*

⏳ La **première mise en ligne prend 1 à 3 minutes**. Patience. Tu peux rafraîchir la page Settings → Pages, un encart vert apparaîtra quand c'est prêt.

---

## ÉTAPE 4 — Vérifier que tout fonctionne

### ✅ Le site est en ligne
Ouvre : **https://vincenthayot-a11y.github.io/les-minis-de-caroline/**

Tu devrais voir le site complet. Teste :
- Le scroll
- Les liens du menu (Approche, Bénéfices, Activités…)
- Les boutons WhatsApp (qui doivent ouvrir WhatsApp avec un message pré-rempli)
- La lightbox de la galerie (clic sur une photo)

### ✅ L'image de partage fonctionne
Va sur **https://www.opengraph.xyz/**
Colle ton URL : `https://vincenthayot-a11y.github.io/les-minis-de-caroline/`
Tu dois voir l'aperçu avec la photo aquapony et le titre **Les Minis de Caroline · Un poney pour grandir**.

C'est cet aperçu qui apparaîtra quand quelqu'un partagera le lien sur **WhatsApp, Facebook, Instagram, LinkedIn, SMS**.

### ✅ Les données structurées sont valides
Va sur **https://search.google.com/test/rich-results**
Colle ton URL.
Tu dois voir : *« 1 valid item detected · SportsActivityLocation »*

C'est ce qui permettra à Google d'afficher ton activité comme un commerce local martiniquais.

---

## ÉTAPE 5 — Référencement Google

### a) Soumettre le site à Google Search Console

1. Va sur **https://search.google.com/search-console**
2. Connecte-toi avec un compte Google
3. Clique **« Ajouter une propriété »** → **« Préfixe d'URL »**
4. Colle : `https://vincenthayot-a11y.github.io/les-minis-de-caroline/`
5. Pour valider la propriété, GitHub Pages ne supporte pas l'upload du fichier HTML de validation, donc choisis la méthode **« Balise HTML meta »** :
   - Google te donne une balise du type `<meta name="google-site-verification" content="ABC123...">`
   - **Reviens me voir avec cette balise**, je te l'intègre dans le `<head>` du site
   - Tu réuploades le nouveau `index.html` sur GitHub
   - Tu retournes sur Search Console et tu cliques **« Vérifier »**
6. Une fois validé, va sur **« Sitemaps »** dans le menu de gauche
7. Soumets : `sitemap.xml`

Google commencera à indexer le site sous quelques jours.

### b) Créer une fiche Google My Business *(TRÈS recommandé pour le SEO local)*

Une fiche Google My Business est **le levier #1 pour le SEO local** d'une association ou d'un commerce. Elle apparaît dans Google Maps et sur la droite des résultats de recherche locaux.

1. Va sur **https://business.google.com/**
2. Crée la fiche au nom **« Les Minis de Caroline »**
3. **Adresse** : Pointe Roseau, Le Robert, 97231 Martinique
4. **Catégorie principale** : *« Centre équestre »* ou *« Association »*
5. **Téléphone** : 0696 74 69 00
6. **Site web** : `https://vincenthayot-a11y.github.io/les-minis-de-caroline/`
7. **Photos** : uploade les meilleures du dossier
8. **Description** : tu peux reprendre celle du site
9. Google demandera une **vérification par carte postale** (carte avec un code envoyée à l'adresse) — compte ~10 jours d'attente

---

## 🎨 Brancher un vrai nom de domaine plus tard

Quand tu auras un nom de domaine type **lesminisdecaroline.fr**, **.com** ou **.mq**, tu pourras obtenir une URL beaucoup plus propre :

1. **Achète le domaine** chez OVH, Gandi, Cloudflare, ou ton registrar préféré
2. **Configure les DNS du domaine** pour pointer vers GitHub Pages :
   - 4 enregistrements de type **A** vers ces IP :
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - 1 enregistrement **CNAME** : `www` → `vincenthayot-a11y.github.io`
3. **Sur GitHub** : Settings → Pages → Custom domain → tape `lesminisdecaroline.fr` → Save
4. **Coche « Enforce HTTPS »** (apparaît après ~10 min, le temps que Let's Encrypt génère le certificat)
5. **Reviens me voir avec le nouveau domaine**, je te referai un search-replace dans tous les fichiers (canonical, og, schema, sitemap, robots, README) pour que tout pointe vers le bon endroit.

Le site reste hébergé gratuitement sur GitHub, juste avec une URL beaucoup plus brandée.

---

## 🔄 Pour modifier le site plus tard

Le plus simple, sans utiliser Git :

1. Va sur le repo : `https://github.com/vincenthayot-a11y/les-minis-de-caroline`
2. Clique sur le fichier à modifier (ex: `index.html`)
3. Clique sur l'icône **crayon** en haut à droite (« Edit this file »)
4. Modifie ce que tu veux
5. En bas de la page, **« Commit changes »**
6. Le site est mis à jour automatiquement sous ~1 minute

Ou — plus pratique pour les grosses modifs — tu reviens me voir avec les changements et je te génère une nouvelle version du fichier que tu uploaderais en remplacement.

---

## 📊 Statistiques de visite *(bonus, gratuit)*

Pour savoir combien de personnes visitent ton site, tu peux ajouter :
- **Plausible** ou **Umami** (alternatives respectueuses de la vie privée à Google Analytics)
- **Google Analytics** classique
- **Cloudflare Web Analytics** (gratuit, simple, RGPD-friendly)

Préviens-moi quand tu veux l'ajouter, c'est 3 lignes de code à insérer.

---

**Tu es paré.** Tu as tout pour publier proprement, suivre l'indexation et faire grandir progressivement la visibilité du site 🎯
