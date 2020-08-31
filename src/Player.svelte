<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();
  export let name;
  export let points;

  var toggleScoreFieldValue = true;

  var toggleScoreField = () => {
    toggleScoreFieldValue = !toggleScoreFieldValue;
  };

  let addPoints = () => {
    points += 1;
  };

  let deletePoints = () => {
    points -= 1;
  };
</script>

<style>

</style>

<main>
  <div class="card">
    <h3>Name : {name}</h3>
    <h4>Points: {points}</h4>
    <button class="btn btn-sm" on:click={toggleScoreField}>
      {#if toggleScoreFieldValue}&#9758;{:else}&#9756;{/if}
    </button>
    {#if toggleScoreFieldValue}
      <!-- <input type="number" bind:value={points} /> -->
      <button class="btn btn-success btn-sm" on:click={addPoints}>
        +&#10102;
      </button>
      <button class="btn btn-danger btn-sm" on:click={deletePoints}>
        -&#10102;
      </button>
    {/if}
    <br />
    <br />
    <button
      class="btn btn-danger btn-sm"
      on:click={() => dispatch('deleteplayer', name)}>
      &#x1f5d1;
    </button>
  </div>
</main>
