<script>
  import Cell from './Cell.svelte';

  const handleSubmit = e => {
    e.preventDefault();
    console.log('submit word', e.target);
  };

  const handleClick = (e, letter) => {
    e.preventDefault();
    console.log('click cell: ', letter);
  };
</script>

<section>
  <form on:submit={handleSubmit}>
    <input type="text" name="word" id="word" />
  </form>
  <Cell {handleClick} letter={'j'} />
  <button>Delete</button>
  <button>Refresh</button>
  <button>Enter</button>
</section>
