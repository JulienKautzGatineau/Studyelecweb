# Mettre le site Study Elec en ligne

Guide pas-à-pas pour publier le site gratuitement, via **GitHub** (stockage du code) + **Vercel** (hébergement). Pas besoin de terminal, tout se fait dans le navigateur.

---

## Avant de commencer

Tu vas créer deux comptes gratuits (si ce n'est pas déjà fait) :

1. **GitHub** — https://github.com/signup
2. **Vercel** — https://vercel.com/signup (clique sur "Continue with GitHub")

Garde un onglet ouvert sur chaque pendant toute la procédure.

---

## Étape 1 — Uploader le site sur GitHub (5 min)

1. Connecte-toi sur **https://github.com**
2. En haut à droite, clique sur le **+** puis **New repository**
3. Remplis le formulaire :
   - **Repository name** : `study-elec-site`
   - **Public** (coche cette case)
   - Coche **Add a README file**
   - Clique **Create repository**
4. Sur la page du repo qui s'affiche, clique **Add file → Upload files**
5. Glisse-dépose le fichier **`index.html`** (depuis le dossier `study-elec` que je t'ai créé)
6. Tout en bas, clique sur le bouton vert **Commit changes**

✅ Le site est maintenant stocké sur GitHub.

> **Astuce** : si tu veux que les **3 versions** (V1, V2 dark tech, V3 éditorial) soient accessibles, glisse-dépose aussi les dossiers `version-2-dark-tech/` et `version-3-editorial/` ainsi que `presentation.html`. Pour uploader un dossier, il faut le faire par glisser-déposer depuis l'explorateur de fichiers.

---

## Étape 2 — Connecter Vercel à GitHub (2 min)

1. Va sur **https://vercel.com**
2. Clique **Sign up** → **Continue with GitHub** (utilise le compte GitHub que tu viens de créer / connecter)
3. Vercel te demande d'autoriser l'accès à tes dépôts → clique **Authorize Vercel**

---

## Étape 3 — Déployer le site (2 min)

1. Sur le dashboard Vercel, clique **Add New… → Project**
2. Dans la liste, tu vois ton dépôt `study-elec-site` → clique **Import**
3. Vercel détecte automatiquement que c'est un site HTML. Ne touche à rien, laisse les réglages par défaut.
4. Clique **Deploy**

⏱️ Attends ~30 secondes. Une animation confetti s'affiche quand c'est terminé.

✅ **Ton site est en ligne** à une adresse du type :
`https://study-elec-site.vercel.app`

Clique sur l'aperçu pour le voir en direct.

---

## Étape 4 — (Optionnel) Ajouter un nom de domaine personnalisé

Si tu veux `www.study-elec.fr` au lieu de `study-elec-site.vercel.app` :

1. Achète un domaine sur **OVH**, **Gandi** ou **Cloudflare** (prix : ~10-15 €/an)
2. Sur Vercel, dans ton projet → onglet **Settings → Domains**
3. Tape `study-elec.fr` → **Add**
4. Vercel affiche deux enregistrements DNS à configurer :
   - Un **A record** vers `76.76.21.21`
   - Un **CNAME** `www` vers `cname.vercel-dns.com`
5. Va dans ton registrar (OVH/Gandi), dans la zone DNS du domaine, et colle les deux enregistrements
6. Reviens sur Vercel — au bout de quelques minutes à quelques heures, Vercel coche automatiquement ✓ **Valid Configuration** et active le **HTTPS gratuit**

---

## Mettre à jour le site plus tard

Dès que tu modifies `index.html` sur GitHub (ou que tu uploades une nouvelle version via **Add file → Upload files**), **Vercel redéploie automatiquement** en moins d'une minute. Pas besoin de retoucher quoi que ce soit.

---

## En cas de souci

- **Le site ne s'affiche pas** → vérifie que le fichier à la racine du dépôt s'appelle exactement `index.html` (tout en minuscules)
- **Le logo ne s'affiche pas** → c'est un SVG intégré dans le HTML, il n'y a pas de fichier image à uploader en plus
- **Je veux revenir à une version précédente** → sur Vercel onglet **Deployments**, clique sur les **⋯** d'un ancien déploiement → **Promote to Production**

---

## Récap des coûts

| Service | Coût |
|---|---|
| GitHub (dépôt public) | **Gratuit** |
| Vercel (hébergement + HTTPS + domaine .vercel.app) | **Gratuit** |
| Nom de domaine .fr (OVH/Gandi) — *optionnel* | ~10-15 €/an |

**Total : 0 €** pour un site pro en ligne, 10-15 €/an si tu veux ton propre nom de domaine.
