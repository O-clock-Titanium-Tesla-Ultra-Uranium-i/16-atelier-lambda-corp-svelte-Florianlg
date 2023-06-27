<script>
    // Export permet de transformer ces variables en attributs du composant
    export let first_name = '';
    export let last_name = '';
    export let email = '';
    export let phone_number = '';
    export let rating = '';
    export let status = '';
</script>


<!-- Affichage détaillé d'un contact -->
<div class="{status}">
    <b><i class="fa-solid fa-circle-user"></i> {first_name} {last_name}</b>
    <hr>
    <p><i class="fa-solid fa-envelope"></i> {email}</p>
    <p><i class="fa-solid fa-phone"></i> {phone_number}</p>
    <hr>
    <span><i class="fa-solid fa-star"></i>{rating}</span>
</div>


<style>
    div {
        background-color: white;
        border-radius: 5px;
        margin: 1em;
        display: flex;
        flex-direction: column;
        padding: 1em;
        width: 250px;
        box-shadow: 0 0 4px 0 rgb(105, 105, 105);
    }
    b {
        font-size: 1.5em;
    }
    hr {
        width: 100%;
    }
    span {
        margin-left: auto;
    }
</style>