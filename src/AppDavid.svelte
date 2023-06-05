<script>
  import GameBoard from './Game-board.svelte';
  let points = 20;

  function resetGame() {
    points = 0;
    location.reload();
  }
</script>

<div class="row">
  <div class="col text-center">
    <h1>MTG Counter App</h1>
  </div>
</div>

<div class="container text-center">
  <div class="row">
    <div class="col">
      <GameBoard {points} color="red" />
    </div>
    <div class="col">
      <GameBoard {points} color="blue" />
    </div>
  </div>
</div>

<button on:click={resetGame} type="button" class="btn btn-warning"
  >Reset Game</button
>
<button
  on:click={resetGame}
  type="button"
  class="btn btn-success">New Game</button
>

<style>
  button {
    margin-top: 2rem;
    width: 99%;
    margin: 5px auto;
    font-size: 0.8rem;
    font-weight: bold;
    padding: 2px;
  }

  /* button.hidden {
    display: none;
  } */
</style>
