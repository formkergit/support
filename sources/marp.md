---
marp: true
theme: default
paginate: true
header: MARP
footer: Présentation avec MARP
---

# MARP

## Outil de présentation en markdown

[https://marp.app/](https://marp.app/)

---

Installer l'extension **Marp for VS Code** dans **VSCODE**

---

# Entête du fichier de markdown de présentation

```
---
marp: true
theme: default
paginate: true
header: Texte entête de la présentation
footer: Texte pied de page de la présentation
---
```

---

# Themes

## 3 themes disponibles

- default
- gaia
- uncover 

[https://github.com/marp-team/marp-core/tree/main/themes](https://github.com/marp-team/marp-core/tree/main/themes)

---

# Dark theme

Ajouter la classe **invert** pour avoir le theme utlisé en **dark**

```
class: invert
```

---

# Pagination

```
paginate: true
```

---

# Slides

Les slides sont séparées par `---`

---

# Image

![Marp](./marp.png)

![width:50px](./marp.png)

![width:200px height:50px](./marp.png)

![w:64 h:64](./marp.png)

[https://marpit.marp.app/image-syntax]()

---

# Image Filtre

![blur](./marp.png)

![drop-shadow](./marp.png)


---

# Plusieurs backgrounds

---

![bg](https://ph.loremipsums.org/300x200/004080/FFFFFF/svg?text=A)
![bg](https://ph.loremipsums.org/300x200/0080C0/FFFFFF/svg?text=A)
![bg](https://ph.loremipsums.org/300x200/80FFFF/FFFFFF/svg?text=A)

---


![bg vertical](https://ph.loremipsums.org/800x60/004080/FFFFFF/svg?text=A)
![bg vertical](https://ph.loremipsums.org/800x60/0080C0/FFFFFF/svg?text=A)
![bg vertical](https://ph.loremipsums.org/800x60/80FFFF/FFFFFF/svg?text=A)

---

Image en background postionné en fonction du texte à gauche

![bg left:40% 80%](https://marp.app/assets/marp.svg)

---

![bg right](https://lipsum.app/random/800x600)

# Titre texte image

Image en background postionné en fonction du texte à droite

---

![bg right](https://picsum.photos/720?image=3)
![bg](https://picsum.photos/720?image=20)

# Plusieurs background

Texte d'accompagnement des images.

---

## Class pour **centrer** les titres et textes dans toutes les slides fonctionne avec les themes **gaia** et **uncover**

```
class: lead
```

---

# Emoji

:smile: :heart: :sparkles:

😄😉​😂​😇​

[https://emojikeyboard.top/fr/](https://emojikeyboard.top/fr/)