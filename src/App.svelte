<script>
  import Navbar from "./Navbar.svelte";
  import Player from "./Player.svelte";
  import AddPlayer from "./AddPlayer.svelte";
  let players = [
    {
      name: "Vaibhav",
      points: 9,
    },
  ];

  function addPlayerFunc(e) {
    const newPlayer = e.detail;
    players = [...players, newPlayer];
  }

  function deletePlayer(e) {
    players = players.filter((player) => player.name !== e.detail);
  }
</script>

<style>
  main {
    padding: 10px;
  }
</style>

<main>
  <Navbar />
  <div class="container">
    <AddPlayer on:addplayer={addPlayerFunc} />
    {#each players as player}
      <Player
        name={player.name}
        points={player.points}
        on:deleteplayer={deletePlayer} />
    {:else}
      <center>
        <h3>No Players &#9785;</h3>
      </center>
    {/each}
  </div>
</main>
