# win.css
## Résumé
Un mini framework pour générer les feuilles de styles
## Illustration en ligne
Cliquer sur ce [lien](https://alhasnecode.github.io) pour visualiser la demo
## Installation
- Clôner le dépôt sur votre machine `$ git clone https://github.com/alhasnecode/win.css.git`
- Copier le chemin absolu du fichier demo/demo.html et coller le sur la barre d'URL de votre navigateur pour visualiser la demo
## Utilisation
#### Utilisation de la version CSS prête
- Ajouter le lien vers le fichier css/win.css à votre document HTML
- Utiliser les noms de classes définis dans ce fichier avec les éléments de votre document HTML
#### Utilisation de la version SCSS
Vous pouvez vous servir des mixins des différents composants fournis avec la version SCSS dans le répertoire scss/mixins.
##### Exemple d'utilisation avec le composant buttons
- Créer un fichier custom.scss
- Importer le fichier des mixins du composant buttons `@import 'mixins/buttons_mixins'`
- Définir le style de votre boutton avec les mixins fournis
```
.nomDeVotreClasse{
  @include btn_structure(10px, 0, inline-block, 40px, auto, 5px);
  @include btn_gradient(to bottom, #fceabb 0%,#fccd4d 50%,#f8b500 51%,#fbdf93 100%);
}
 ```
 - Générer le fichier .css à utiliser dans votre document HTML avec la commande `$ sass custom.scss:custom.css`
 ## Personnalisation
 Vous pouvez personnaliser la définition des classes générées par défaut dans le framework en deux étapes
 - Modifier les valeurs des différentes variables dans le fichier `scss/vars`
 - Regénérer le fichier css principal avec la commande `$ sass scss/build.scss:css/win.css`
