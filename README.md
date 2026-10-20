# Shaarli Geccko Dark

Un thème sombre et moderne pour [Shaarli](https://github.com/shaarli/Shaarli) (testé avec Shaarli 0.16.9).

Basé sur le thème `default` de Shaarli : la structure HTML et le JavaScript sont inchangés, tout le style est
dans une feuille dédiée, `css/dark.css`, chargée après les styles d'origine.

## Points forts

- Fond bleu nuit, panneaux gris-bleu, accent vert émeraude (`#34d399`)
- Menu en verre dépoli, liens en cartes arrondies, tags en pastilles
- Liens privés soulignés en ambre, épinglés en bleu
- Formulaires, cases à cocher, autocomplétion, alertes, pagination, nuage de tags, mur d'images, Daily et Markdown
  adaptés au mode sombre
- Icônes de plugins (QR code, archive.org…) inversées pour rester lisibles
- Largeur de contenu unique et centrée sur toutes les pages (1100px par défaut)
- Responsive ; impression en clair ; respecte `prefers-reduced-motion`

## Installation

Depuis la racine de votre installation Shaarli :

```bash
git clone https://github.com/h2tp/Shaarli-Geccko-Dark.git tpl/dark
```

Puis **Outils → Configurer votre Shaarli → Thème → `dark`**,
ou `"theme": "dark"` dans `data/config.json.php`.

> Si votre serveur web sert le dossier `tpl/`, supprimez `tpl/dark/.git` après le clonage
> (ou bloquez l'accès aux dossiers `.git`), pour ne pas exposer l'historique git.

## Personnalisation

Les couleurs et la largeur sont des variables CSS en haut de `css/dark.css` :

```css
:root {
  --main-color: #34d399;      /* accent */
  --dark-main-color: #10b981; /* accent au survol */
  --background-color: #0d1017;
  --dk-page-width: 1100px;    /* largeur du contenu */
}
```

Le plugin `default_colors` de Shaarli fonctionne aussi, ainsi que `data/user.css`.

## Mise à jour de Shaarli

Le thème est une copie des templates `default`. Lors d'une montée de version de Shaarli, recopiez les nouveaux
templates de `tpl/default` en conservant `css/dark.css` et la ligne qui le charge dans `includes.html` :

```html
<link type="text/css" rel="stylesheet" href="{$asset_path}/css/dark.css?v={$version_hash}#" />
```

## Licence

Comme Shaarli, ce thème est distribué sous licence zlib/libpng — voir [COPYING](COPYING).
