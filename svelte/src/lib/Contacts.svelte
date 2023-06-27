<script>
    import Contact from './Contact.svelte'
    import DetailledContact from './DetailledContact.svelte'

    let contacts = [];

    // Fonction d'appel à l'api
    export const getContacts = async () => {
        const r = await fetch(import.meta.env.VITE_URL_DIRECTUS + "items/contacts", {
            headers: {
                'Authorization': 'Bearer ' + window.localStorage.getItem('token')
            },
        })
        const json = await r.json()
        contacts = json.data
    }
</script>


<section>
    <!-- Si la liste est vide, affiche un message et un bouton de chargement -->
    {#if contacts.length === 0 }
        <p>Aucun contact affiché</p>
        <button on:click={getContacts}>Charger la liste</button>
    {/if}

    <!-- Boucle sur la liste des contacts -->
    {#each contacts as contact} 
        <!-- Ajoute un contact et fournit le nom et prénom en attribut  -->
        <Contact first_name={contact.first_name} last_name={contact.last_name}/>
        
        <!-- Bonus : affiche un contact déaillé 
        Utilisation de l'éclatement des propriétés https://svelte.dev/tutorial/spread-props -->
         <DetailledContact {...contact}/>
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