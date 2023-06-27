<script>
    // Export permet de transformer ces variables en attributs du composant
    export let first_name = '';
    export let last_name = '';
</script>


<!-- Affichage d'un contact simplement -->
<p class="contact">{first_name} {last_name}</p>


<style>
    p {
        padding: 1em 3em;
        background-color: white;
        border-radius: 5px;
        margin: 1em;
    }
</style>