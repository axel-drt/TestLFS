# Git Large File Storage (LFS)

## LFS, c'est quoi ?

Git Large File Storage (LFS) remplace les fichiers volumineux (échantillons audio, vidéos, datasets, graphiques) par des pointeurs textuels dans Git, tandis que les contenus des fichiers sont stockés sur un serveur distant comme GitHub.com ou GitHub Enterprise.

🔗 [Site officiel de Git LFS](https://git-lfs.com/)

### Est-ce obligatoire pour un projet Unity ?
Oui. Sinon, Git renverra une erreur du type :
> "blablabla c trop lourd mon reuf tu peux pas push"

---

## Comment installer Git LFS ?

### 📌 Prérequis
- Installer **GitHub Desktop** et **Git Bash**

### 🛠 Étape 1 : Créer un repo GitHub et ajouter le projet Unity

### 🛠 Étape 2 : Initialiser LFS
```bash
$ git lfs install
Updated Git hooks.
Git LFS initialized.
```

### 🛠 Étape 3 : Ajouter les extensions à suivre avec LFS
```bash
$ git lfs track "*.unity"
Tracking "*.unity"

$ git lfs track "*.fbx"
Tracking "*.fbx"

$ git lfs track "*.prefab"
Tracking "*.prefab"
```

### 🛠 Étape 4 : Commit et push des fichiers de suivi
```bash
$ git add .gitattributes
$ git commit -m "Add - Tracking files with LFS"
$ git push
```
Après cela, on peut utiliser Git normalement. ✅

---

## 💰 Combien ça coûte ?

Les comptes GitHub gratuits avec Git LFS bénéficient de **1 GiB de stockage** et **1 GiB de bande passante** gratuits par mois. Si ces quotas sont dépassés, il est possible d'acheter des quotas supplémentaires.

🔗 [Infos officielles sur la gestion du stockage et de la bande passante](https://docs.github.com/en/enterprise-cloud@latest/repositories/working-with-files/managing-large-files/about-storage-and-bandwidth-usage)

🔗 [Infos officielles sur la facturation de Git LFS](https://docs.github.com/en/billing/managing-billing-for-your-products/managing-billing-for-git-large-file-storage/about-billing-for-git-large-file-storage)

### 📊 Limites de taille des fichiers selon l'abonnement
| Plan | Taille max fichier |
|------|------------------|
| **GitHub Free** | 2 GB |
| **GitHub Pro** | 2 GB |
| **GitHub Team** | 4 GB |
| **GitHub Enterprise Cloud** | 5 GB |

### 💵 Tarification des packs de stockage supplémentaires

- **1 pack = 5 $/mois** pour **50 GiB** de stockage et **50 GiB** de bande passante.
- Il est possible d'acheter plusieurs packs (ex: **3 packs = 150 GiB pour 15 $/mois**).

---

## 📌 Les plans GitHub

### **GitHub Free**
✅ Collaboration illimitée sur des dépôts publics et privés
✅ 500 Mo de stockage GitHub Packages
✅ 120 heures de GitHub Codespaces / mois
✅ 15 Go de stockage GitHub Codespaces / mois
✅ 2,000 minutes GitHub Actions / mois
✅ GitHub Pages pour dépôts publics
💰 **Prix : Gratuit**

### **GitHub Team**
✅ Toutes les fonctionnalités de GitHub Free
✅ Support GitHub par email
✅ 3,000 minutes GitHub Actions / mois
✅ 2 Go de stockage GitHub Packages
✅ 180 heures de GitHub Codespaces / mois
✅ 20 Go de stockage GitHub Codespaces / mois
✅ Outils avancés (ex: code owners, branches protégées)
✅ GitHub Pages pour dépôts privés
✅ Wikis et repository insights graphs
💰 **Prix : 4 $/mois par utilisateur**

### **GitHub Enterprise**
✅ Toutes les fonctionnalités de GitHub Team
✅ Support GitHub Enterprise
✅ Contrôles de sécurité, conformité et déploiement avancés
✅ Authentification SAML Single Sign-On
✅ Provisioning d'accès SAML ou SCIM
✅ GitHub Connect
✅ Option GitHub Advanced Security
✅ 50,000 minutes GitHub Actions / mois
✅ 50 Go de stockage GitHub Packages
✅ SLA 99.9% de disponibilité
✅ Gestion centralisée des politiques et facturation
✅ Hébergement des données dans une région spécifique
💰 **Prix : 21 $/mois par utilisateur**

---

## 🚀 Et GitLab dans tout ça ?

Une autre veille serait nécessaire pour détailler, mais globalement :

### 💻 Hébergement **en local**
- Nécessite une bonne infrastructure et un serveur externe pour LFS

### ☁ Hébergement **sur un serveur loué**
- Peut être **moins cher** que GitHub
- Mais plus complexe à gérer

---

## 🔎 Conclusion

Sachant que :
- Les quotas de stockage et de bande passante pour Git LFS sont partagés au niveau de l'organisation sur **GitHub Team**
- Seul l'administrateur peut gérer l'achat des packs supplémentaires

➡ **La solution la plus rentable** pour nous serait **GitHub Team** à **4 $/mois par utilisateur** (soit **48 $/an**) avec un éventuel achat de **data packs** si nécessaire. 🚀
