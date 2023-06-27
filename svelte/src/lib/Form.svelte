<script>
    // On préremplie les valeurs pour ne pas avoir à les taper dans le navigateur ;)
    let email = "bot@example.com";
    let pwd = "1234";


    // Méga Bonus
    // Crée un dispatcher pour remonter des événements à App
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();


    const onSubmit = async (event) => {
        // On oublie pas que le navigateur veut recharger la page à la soumission d'un formulaire...
        // Du coup on le bloque
        event.preventDefault()

        // Les valeur sont 'bindées' par Svelte, donc j'ai rien à faire !
        // Ca devient presque magique :)
        console.log(email, pwd);

        // Récupère le token via l'api
        let token = await getToken();

        // Stocke le token dans le localstorage
        window.localStorage.setItem('token', token);
    
        // Méga Bonus
        // Génère un événement submit au niveau du composant
        dispatch('submit');
    }

    // Fonction d'authentification à l'api
    async function getToken () {
        const r = await fetch(import.meta.env.VITE_URL_DIRECTUS + "auth/login", {
            method: "POST",
            headers: {
                'Content-Type': 'application/json'
            },
            body: JSON.stringify({
                email: email,
                password: pwd
            })
        })

        // Extrait le json de la réponse
        const json = await r.json()
        // Extrait le token de la réponse
        return json.data.access_token
    }
</script>


<!-- Formulaire de connexion -->
<form on:submit={onSubmit}>
    <label for="email">Email</label>
    <input type="mail" id="email" name="email" bind:value={email}>
    <label for="pwd">Mot de passe</label>
    <input type="password" id="pwd" name="password" bind:value={pwd}>
    <button>Se connecter</button>
</form>


<style>
    form {
        background: white;
        padding: 2em;
        z-index: 2;
        box-shadow: 0 0 6px 0 rgb(105, 105, 105);
        position: sticky;
        top: 0;
    }
</style>