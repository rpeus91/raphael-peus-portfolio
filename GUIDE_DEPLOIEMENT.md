# Guide de déploiement du portfolio

## Option 1 : GitHub Pages (Recommandé - Gratuit)

### Étapes détaillées :

1. **Créer un compte GitHub** (si vous n'en avez pas)
   - Allez sur https://github.com
   - Créez un compte gratuit

2. **Installer Git** (si ce n'est pas déjà fait)
   - Téléchargez : https://git-scm.com/download/win
   - Installez avec les options par défaut

3. **Créer un nouveau dépôt sur GitHub**
   - Cliquez sur le "+" en haut à droite → "New repository"
   - Nom : `portfolio` ou `raphael-peus-portfolio`
   - Description : "Portfolio personnel - Data analyst / Data scientist"
   - Cochez "Public"
   - **Ne cochez PAS** "Initialize with README"
   - Cliquez sur "Create repository"

4. **Ajouter vos fichiers au dépôt** (via Git en ligne de commande)

   Ouvrez PowerShell dans le dossier de votre portfolio et exécutez :

   ```powershell
   # Initialiser Git
   git init
   
   # Ajouter tous les fichiers
   git add .
   
   # Créer le premier commit
   git commit -m "Initial commit - Portfolio"
   
   # Ajouter le dépôt distant (remplacez USERNAME par votre nom d'utilisateur GitHub)
   git remote add origin https://github.com/USERNAME/portfolio.git
   
   # Pousser les fichiers
   git branch -M main
   git push -u origin main
   ```

5. **Activer GitHub Pages**
   - Allez dans votre dépôt sur GitHub
   - Cliquez sur "Settings" (en haut)
   - Dans le menu de gauche, cliquez sur "Pages"
   - Sous "Source", sélectionnez "Deploy from a branch"
   - Choisissez "main" comme branche et "/ (root)" comme dossier
   - Cliquez sur "Save"
   - Attendez 1-2 minutes

6. **Votre site sera accessible à :**
   - `https://USERNAME.github.io/portfolio/`

### ⚠️ Note importante sur les fichiers volumineux :
- GitHub a une limite de 100 MB par fichier
- Les vidéos (`*.mp4`) peuvent être trop lourdes
- **Solution** : Utilisez des services externes pour les vidéos (YouTube, Vimeo) ou compressez-les

---

## Option 2 : Netlify (Très simple - Drag & Drop)

### Étapes :

1. **Aller sur Netlify**
   - Allez sur https://www.netlify.com
   - Créez un compte gratuit (vous pouvez vous connecter avec GitHub)

2. **Déployer votre site**
   - Sur la page d'accueil, faites glisser votre dossier "Portfolio" dans la zone "Drag and drop your site output folder here"
   - OU cliquez sur "Add new site" → "Deploy manually" → glissez le dossier

3. **Votre site sera accessible immédiatement**
   - Netlify génère une URL automatique : `https://random-name-123.netlify.app`
   - Vous pouvez personnaliser le nom dans les paramètres

### Avantages Netlify :
- ✅ Très rapide (quelques secondes)
- ✅ Pas besoin de Git
- ✅ Supporte les fichiers volumineux (vidéos, PDFs)
- ✅ HTTPS automatique
- ✅ Vous pouvez changer le nom de domaine

---

## Option 3 : Vercel (Alternative simple)

1. Allez sur https://vercel.com
2. Créez un compte (connectez-vous avec GitHub)
3. Cliquez sur "Add New Project"
4. Importez votre dépôt GitHub OU uploadez le dossier
5. Cliquez sur "Deploy"

---

## Recommandation

**Pour débuter rapidement** : Utilisez **Netlify** (drag & drop, 2 minutes)

**Pour un déploiement professionnel** : Utilisez **GitHub Pages** (gratuit, fiable, bon pour le CV)

---

## Personnaliser l'URL (optionnel)

### GitHub Pages :
- Dans les paramètres du dépôt → Pages
- Vous pouvez utiliser un nom de domaine personnalisé

### Netlify :
- Dans Site settings → Change site name
- Vous pouvez choisir un nom personnalisé : `raphael-peus-portfolio.netlify.app`

---

## Mettre à jour le site

### GitHub Pages :
```powershell
git add .
git commit -m "Mise à jour du portfolio"
git push
```
Le site se met à jour automatiquement en 1-2 minutes.

### Netlify :
- Glissez simplement le nouveau dossier
- OU connectez votre dépôt GitHub pour un déploiement automatique

