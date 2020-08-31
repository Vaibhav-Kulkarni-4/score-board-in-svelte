<script>
  import { createEventDispatcher } from "svelte";

  let player = {
    name: "",
    points: 0,
  };

  const dispatch = createEventDispatcher();
  const onSubmitForm = (e) => {
    dispatch("addplayer", player);
    player = {
      name: "",
      points: 0,
    };
  };
</script>

<form on:submit|preventDefault={onSubmitForm} class="grid-3">
  <input
    type="text"
    id="playerName"
    placeholder="Player Name"
    bind:value={player.name} />
  <input type="number" placeholder="Player Points" bind:value={player.points} />
  <input type="submit" class="btn btn-primary" value="Add Player" />
</form>
