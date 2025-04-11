---
title: developement
menu:
  main:
    weight: 400
---
# Rédiger du Contenu en Markdown

Cecil prend en charge la syntaxe [Markdown](https://cecil.app/documentation/content/#markdown) dans les fichiers `.md` ainsi que les [métadonnées](https://cecil.app/documentation/content/#front-matter) pour définir des variables.

**Table des matières :**

[toc]

```markdown
[toc]
```

## Style en ligne

Le texte peut être **gras**, _italique_, ou ~~barré~~.

```markdown
Le texte peut être **gras**, _italique_, ou ~~barré~~.
```

Vous pouvez [lier à une page](/about.md) ou [à une autre page](page:index).

```markdown
Vous pouvez [lier à une page](/about.md) ou [à une autre page](page:index).
```

Vous pouvez mettre en évidence du `code en ligne` avec des accents graves.

```markdown
Vous pouvez mettre en évidence du `code en ligne` avec des accents graves.
```

## Comment structurer une page

Cecil utilise automatiquement le nom du fichier comme titre, mais vous pouvez également définir un titre et d'autres variables dans les [métadonnées](https://cecil.app/documentation/content/#front-matter).

Vous pouvez structurer le contenu en utilisant un titre. Les titres en Markdown sont indiqués par un nombre de `#` au début de la ligne.

```markdown
---
title: exemple
description: démonstration de cecil
---

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

## Titre

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
```

## Image

Les images utilisent le support intégré d'optimisation des ressources de Cecil.

![Cecil favicon](/favicon.png "Cecil favicon")

```markdown
![Cecil favicon](/favicon.png "Cecil favicon")
```

Cecil recherche les images dans les dossiers `assets/` et `static/`, mais le chemin relatif est également pris en charge :

```markdown
![Cecil favicon](../assets/favicon.png "Cecil favicon")

```
## Liste

* Liste non ordonnée
* Liste non ordonnée
* Liste non ordonnée

1. Liste ordonnée
2. Liste ordonnée
3. Liste ordonnée

* Niveau 1
  * Niveau 2
  * Niveau 2
    * Niveau 3
    * Niveau 3

## Bloc de citation

> Ceci est un bloc de citation, souvent utilisé pour citer une autre personne ou un document.
>
> Les blocs de citation sont indiqués par un `>` au début de chaque ligne.

```markdown
> Ceci est un bloc de citation, souvent utilisé pour citer une autre personne ou un document.
>
> Les blocs de citation sont indiqués par un `>` au début de chaque ligne.
```

## Bloc de code

Un bloc de code est indiqué par un bloc avec trois accents graves ` ``` ` au début et à la fin. Vous pouvez indiquer le langage de programmation utilisé après les accents graves d'ouverture.

```php
// Code PHP
$config = [
    'title'   => "Mon site web",
    'baseurl' => 'http://localhost:8000/',
];

Builder::create($config)->build();
```

<pre>
```php
// Code PHP
$config = [
    'title'   => "Mon site web",
    'baseurl' => 'http://localhost:8000/',
];

Builder::create($config)->build();
```
</pre>

## Il y a une règle horizontale ci-dessous

---

## Liste de définitions

Premier Terme
: Ceci est la définition du premier terme.

Deuxième Terme
: Ceci est une définition du deuxième terme.
: Ceci est une autre définition du deuxième terme.

## Tableau

| Colonne 1    | Colonne 2          | Colonne 3 |
|:-------------|:-------------------|:----------|
| ok           | bon poisson suédois| sympa     |
| en rupture   | bon et abondant    | sympa     |
| ok           | bons `oreos`       | hmm       |
| ok           | bon `zoute` drop   | miam      |

## Notes

:::
vide
:::

:::info
info
:::

:::tip
conseil
:::

:::important
important
:::

:::warning
avertissement
:::

:::caution
prudence
:::

```markdown
:::info|tip|important|warning|caution
Note ici.
:::
```
