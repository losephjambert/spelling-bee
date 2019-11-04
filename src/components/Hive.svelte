<script>
  import Cell from './Cell.svelte';

  // cell letter stub data
  const letters = ['f', 'i', 'n', 'r', 'c', 'h', 'o'];

  const handleSubmit = e => {
    e.preventDefault();
    console.log('submit word', e.target);
  };

  const handleClick = (e, letter) => {
    e.preventDefault();
    console.log('click cell: ', letter);
  };
</script>

<style>
  section.hive {
    position: relative;
  }
</style>

<section>
  <form on:submit={handleSubmit}>
    <input type="text" name="word" id="word" />
  </form>
  <section class="hive">
    {#each letters as letter, i}
      <Cell {handleClick} {letter} center={i === letters.length - 1} />
    {/each}
  </section>
  <button>Delete</button>
  <button>Refresh</button>
  <button>Enter</button>
</section>
