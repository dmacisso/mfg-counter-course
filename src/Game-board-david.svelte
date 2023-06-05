<script>
  export let color;
  export let points;

  function incrementPoints() {
    points++;
    if (points < 1) {
      console.log(`${color} Wins..`);
    }
  }

  function decrementPoints() {
    points--;
    if (points < 1) {
      console.log(`${color} Wins..`);
    }
  }

  
</script>

<div class="game-board row">
  <div style="border: 3px dotted {color}" class="col">
    <h2 style="color:{color}">Team {color}: {points}</h2>
    <div class="row">
      <div class="col score-btn">
        <button on:click={incrementPoints} class="btn btn-success btn-sm"
          >+</button
        >
      </div>
      <div class="col score-btn">
        <button on:click={decrementPoints} class="btn btn-danger btn-sm"
          >-</button
        >
      </div>
    </div>
  </div>
</div>

<style>
  div.game-board {
    max-width: 400px;
    max-height: 100px;
    /* border: 3px dotted black; */
  }
  button {
    margin-bottom: 1rem;
  }

  
</style>
