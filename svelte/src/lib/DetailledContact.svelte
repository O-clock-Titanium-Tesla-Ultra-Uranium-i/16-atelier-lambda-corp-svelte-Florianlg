<script>
    // Export permet de transformer ces variables en attributs du composant
    export let first_name = '';
    export let last_name = '';
</script>


<!-- Affichage détaillé d'un contact -->
<!-- TODO : ajouter toutes les valeurs dans le HTML -->
<artcile class="">
    <h3><i class="fa-solid fa-circle-user"></i> </h3>
    <p><i class="fa-solid fa-envelope"></i> </p>
    <p><i class="fa-solid fa-phone"></i> </p>
    <span><i class="fa-solid fa-star"></i> </span>
</artcile>


<style>
    artcile {
        background-color: white;
        border-radius: 5px;
        margin: 1em;
        display: flex;
        flex-direction: column;
        padding: 1em;
        width: 250px;
        box-shadow: 0 0 4px 0 rgb(105, 105, 105);
    }
    h3 {
        font-size: 1.5em;
    }
    span {
        margin-left: auto;
    }
</style>