<script>
  const petChoices = ["dog", "cat", "snake", "rat"];
</script>

<div class="select-pet">
  <div class="select-pet-header"></div>
  {#each petChoices as pet}
    <button class="pet-button" value={pet} on:click={() => console.log({ pet })}
      >{pet}</button
    >
  {/each}
</div>

<style>
  .select-pet {
    display: flex;
    flex-wrap: wrap;
    width: 40%;
    height: 300px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 1;
    background-color: rgba(245, 245, 245, 0.737);
    border-radius: 20px;
    overflow: hidden;
  }

  .pet-button {
    width: 50%;
    border: none;
    cursor: pointer;
  }

  .pet-button:hover {
    background-color: rgba(182, 182, 182, 0.737);
  }
</style>
