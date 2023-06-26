<script>
    let email;
    let pwd;

    const onSubmit = async (event) => {
        // TODO : Extraire les valeurs des inputs dans les variables email et pwd
        // TODO : Les afficher dans la console


        // TODO : Récupère le token via l'api
        // et le stocker dans le localstorage

    };

    // Fonction d'authentification à l'api
    async function getToken () {
        // TODO : Ecrire la requête d'authentification à l'api
        
        // L'url de directus se trouve dans les variables d'environnement
        console.log(import.meta.env.VITE_URL_DIRECTUS);
        
        // TODO : Extraire et retourner le token
    }
</script>


<!-- Formulaire de connexion -->
<!-- TODO : brancher la fonction onSubmit sur le formulaire 
Exemple : https://svelte.dev/repl/8eb540552faa4651a398b182fa5cdd48?version=3.24.1 -->
<form>
    <label for="email">Email</label>
    <!-- TODO : brancher la variable email sur l'attribut value (https://svelte.dev/tutorial/text-inputs)-->
    <input type="mail" id="email" name="email">
    <label for="pwd">Mot de passe</label>
    <!-- TODO : brancher la variable pwd sur l'attribut value (https://svelte.dev/tutorial/text-inputs)-->
    <input type="password" id="pwd" name="password">
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