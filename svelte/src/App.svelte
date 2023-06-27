<script>
  import Form from './lib/Form.svelte'
  import Contacts from './lib/Contacts.svelte'

  // Méga Bonus
  // Variable contenant le composant contact pour accéder à ses méthodes
  let compContacts;
  // Fonction déclenchée lors de la soumission du formulaire
  const handleSubmitLogin = () => {
    // Appel de la méthode de chargement des contacts depuis le composant Contacts
    compContacts.getContacts()
  }

  // Méga Bonus : charge automatiquement les contacts si on a un token
  // onMount est équivalent au DOMContentLoaded du DOM, mais pour un composant svelte
  // https://svelte.dev/tutorial/onmount
  import { onMount } from 'svelte'
  onMount(async () => {
    // Appelle automatiquement les récupération des contacts si on a le token
    if ( window.localStorage.getItem('token') !== null ) {
      compContacts.getContacts();
    }
  });
</script>


<main>
  <h2>Lambda corp</h2>
  <Form on:submit={handleSubmitLogin} />
  <Contacts bind:this={compContacts}/>
</main>