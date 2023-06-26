# Frontoffice lambda 

Hey ! Tu es revenu chez nous pour ton deuxième jour ! Je sens qu'on va aller loin ensemble :heart:

J'ai vu la ligne _Svelte_ dans les compétences sur ton CV et ça me paraît cool pour le front de la société. Qu'en penses-tu ?

> *Voix intérieure : Oups ! J'ai peut être abusé sur le CV... Je vais fouiller ma mémoire pour revivre les cours (passionnant) d'O'clock.*

---

Pour rappel, voici tes identifiants, j'ai mis un mois à les retenir perso 😬
- URL : https://maoa39z0.directus.app/
- EMAIL : gloria.marks@example.com
- PWD : 1234

Et pour le compte de dev :
- EMAIL : bot@example.com
- PWD : 1234


## Objectifs 🎯

* Svelte avec un formulaire
* Stocker un token dans le localStorage
* Faire une requête fetch authentifiée avec ce token en le récupérant depuis le localStorage
* Afficher les données récupérées via fetch avec Svelte

## Énonce

> *Voix intérieure : Il y a quelques bouts de code en Svelte, ouf ^^*

On va découper cette nouvelle journée chez Lambda en plusieurs parties.

### Partie 1

* Parcourir le code pour comprendre comment il s'articule
* Identifier les endroits où on gère le formulaire
* Compléter le code pour soumettre le formulaire
* Extraire les valeurs des `<input>` et les afficher dans la console

### Partie 2

* Écrire la requête d'authentification avec les identifiants
* Exécuter et extraire le token de la réponse
* Stocker le token dans le localStorage

### Partie 3

Dans le DOM, il y a un bouton pour afficher les contacts.

* Identifier les endroits où on gère ce bouton
* Extraire le token du localStorage
* Écrire la requête de récupération des contacts avec le token
* Extraire les contacts de la requête
* Voir les contacts s'afficher !

### Bonus 

<details><summary>C'est que du bonus :wink: :arrow_down:</summary>

---

Bon tu as bien bossé ! Si tu veux voir cette partie pour ton troisième jour, tu peux. Mais il faut me promettre de revenir :D 

> *Voix intérieure : Mais pourquoi il croit que je ne vais pas revenir... Que cache cette société ?!? Au pire, tant que je gagne en XP... Bon repos ou code ?*

* Identifier la partie de code qui gère l'affichage des contacts
* Afficher les contacts de façon détaillée avec le composant `DetailledContact`

### Méga bonus

<details><summary>:warning: Attention ça va piquer ! :arrow_down:</summary>

---

Tu sens que Svelte te parle et tu veux aller plus loin ?  
Le but va être de charger directement la liste des contacts après la réception du token.  
Puis dans un second temps, afficher directement la liste si on a déjà le token !

#### #1 Faire remonter l'événement de soumission à App.svelte

Tu vas avoir besoin d'un peu d'aide pour faire ça, regarde [l'exemple sur le site de Svelte](https://svelte.dev/tutorial/component-bindings)

Il y aura un peu de code à mettre dans le composant `Form.svelte` et un peu aussi dans `App.svelte`

Pour vérifier que le submit remonte à `App`, ajoute juste un `console.log` pour l'instant.

Ensuite va voir [l'exemple pour accéder aux méthodes d'un composant](https://svelte.dev/tutorial/component-this)

#### #2 Déclencher la récupération des contacts au chargement de la page

Là aussi tu vas avoir besoin d'aide ^^ [exemple pour le lancement direct au chargement de la page](https://svelte.dev/tutorial/onmount)

Tout va se passer au niveau de `App.svelte`. Si tu as un token dans le localStorage, alors il faut charger les contacts.
  
</details>
  
</details>
