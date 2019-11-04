<script>
  export let handleClick;
  export let value;
</script>

<style>
  button {
    cursor: pointer;
  }
</style>

<button on:click={handleClick}>{value}</button>
