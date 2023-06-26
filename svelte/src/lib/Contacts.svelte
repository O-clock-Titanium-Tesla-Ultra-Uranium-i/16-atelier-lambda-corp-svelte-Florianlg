<script>
    import Contact from './Contact.svelte'
    // import DetailledContact from './DetailledContact.svelte'

    let contacts = [];

    // Fonction d'appel à l'api
    export async function getContacts () {
        // TODO : Extraire le token du localstorage

        // TODO : écrire la requête de récupération des contacts

        // TODO : extraire la liste et la stocker dans la variable contacts
}
</script>


<section>
    <!-- Si la liste est vide, affiche un message et un bouton de chargement -->
    {#if contacts.length === 0 }
        <p>Aucun contact affiché</p>
        <!-- TODO : brancher le click sur le bouton pour appeler la fonction getContacts -->
        <!-- Exemple : https://svelte.dev/tutorial/event-modifiers -->
        <button>Charger la liste</button>
    {/if}

    <!-- Boucle sur la liste des contacts -->
    {#each contacts as contact} 
        <!-- Ajoute un contact et fournit le nom et prénom en attribut  -->
        <!-- TODO : fournit le last_name au composant Contact -->
        <Contact first_name={contact.first_name} />
        
        <!-- Bonus : affiche un contact déaillé -->
    {/each}
</section>


<style>
    section {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        padding: 1em;
    }
</style>