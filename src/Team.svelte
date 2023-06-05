<script>
  export let team;
  export let score;
  export let gameOver;

  function add() {
    score++;
  }

  function minus() {
    score--;
  }
</script>

<div style="border: dashed {team.toLowerCase()} 5px" class="col">
  <h2 class:text-danger={team === 'Red'} class:text-primary={team === 'Blue'}>
    Team {team}: {score}
  </h2>
  <button disabled={gameOver} on:click={add} class="btn btn-success">+</button>
  <button disabled={gameOver} on:click={minus} class="btn btn-danger">-</button>
</div>

<style>
  div.col {
    padding: 20px;
    text-align: center;
  }
</style>
