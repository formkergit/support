---
marp: true
theme: default
paginate: true
header: SSH
footer: Clés SSH pour Services Git
---

# Clés SSH pour Services Git
## Configuration d'Authentification Sécurisée

Configurer les clés SSH pour GitHub, GitLab et Codeberg

---

# Que sont les Clés SSH ?

**Méthode d'authentification cryptographique**

- **Clé publique** → Téléverser sur le service Git
- **Clé privée** → Garder secrète sur votre machine
- **Pas de mots de passe nécessaires** pour les opérations Git
- **Plus sécurisé** que l'authentification HTTPS

---

# Prérequis

**Outils requis :**

```bash
# Vérifier si SSH est installé
ssh -V

# Vérifier si Git est installé
git --version
```

---

# Plateformes prises en charge :

**Linux, macOS, Windows (Git Bash/WSL)**

---

# Générer une clé ED25519 (recommandé)

```
ssh-keygen -t ed25519 -C "votre_email@exemple.com"
```

# Pour les systèmes plus anciens (alternative RSA)

```
ssh-keygen -t rsa -b 4096 -C "votre_email@exemple.com"
```

---

Invites de commande :

- **Emplacement du fichier** : Appuyez sur Entrée (par défaut : ~/.ssh/id_ed25519) , recommandé de donner un nom pour chaque clef généré
- **Phrase de passe** : Facultatif mais recommandé

---

# Démarrer l'agent (Git bash)

```
eval "$(ssh-agent -s)"
```

# Ajouter votre clé privée

```
ssh-add ~/.ssh/id_ed25519
```

---

# Copier dans le presse-papiers (macOS)


# Windows (Git Bash)

```
cat ~/.ssh/id\_ed25519.pub | clip
```

---

# Ajouter à GitHub

1. Aller à **Paramètres** → **Clés SSH et GPG**
2. Cliquer sur **Nouvelle clé SSH**
3. **Titre :** Nom descriptif (par exemple, "Ordinateur Portable Professionnel")
4. **Clé :** Coller votre clé publique
5. Cliquer sur **Ajouter une clé SSH**

**URL :** https://github.com/settings/keys

---

#  Ajouter à GitLab

1. Aller à **Préférences** → **Clés SSH**
2. **Clé :** Coller votre clé publique
3. **Titre :** Nom descriptif
4. **Date d'expiration :** Facultatif
5. Cliquer sur **Ajouter la clé**

**URL :** https://gitlab.com/-/profile/keys

---

# Tester la Connexion

**GitHub :**
```bash
ssh -T git@github.com
# Résultat attendu : "Bonjour username ! Vous avez été authentifié avec succès..."
```

---

# Plusieurs Clés SSH (Avancé)

---

# Éditer ~/.ssh/config

```
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id\_ed25519\_github

Host gitlab.com
  HostName gitlab.com
  User git
  IdentityFile ~/.ssh/id\_ed25519\_gitlab

```

---

# Augmenter votre sécurité 

- Utiliser une **phrase de passe** sur les **clés privées**
- Utiliser l'algorithme **ED25519** (moderne et sécurisé)
- Ne **jamais** partager les **clés privées**
- **Changer** les clés périodiquement
- **Supprimer** les **anciennes** clés des services
- Utiliser des **clés différentes** par appareil