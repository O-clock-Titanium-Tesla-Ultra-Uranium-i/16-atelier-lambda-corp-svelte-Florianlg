
<script>
  // Dans la balise script on va venir écrire toute notre logique en JS
  // On va pouvoir récupérer les variables dans le code HTML en dessous
  let count = 0;
  
  const handleClick = () => {
    count += 1;
  }
</script>
  
<button on:click={handleClick}>
  Clicked {count} {count > 1 ? 'times' : 'time'}
</button>