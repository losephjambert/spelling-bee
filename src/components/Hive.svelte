<script>
  import Cell from './Cell.svelte';
  import Button from './Button.svelte';

  // cell letter stub data
  const letters = ['f', 'i', 'n', 'r', 'c', 'h', 'o'];

  // current word
  let currentWord = [];

  const handleSubmit = e => {
    e.preventDefault();
    console.log('submit word', e.target);
  };

  const addLetter = (e, letter) => {
    e.preventDefault();
    console.log('click cell: ', letter);
    currentWord = [...currentWord, letter];
  };

  const deleteLetter = () => {
    console.log('delete letter');
    const newArray = currentWord.slice(0, -1);
    currentWord = [...newArray];
  };
</script>

<style>
  section.hive {
    position: relative;
  }
</style>

<section>
  <form on:submit={handleSubmit}>
    <input
      type="text"
      name="word"
      id="word"
      bind:value={currentWord}
      value={currentWord.join('')} />
  </form>
  <section class="hive">
    {#each letters as letter, i}
      <Cell handleClick={addLetter} {letter} center={i === letters.length - 1} />
    {/each}
  </section>
  <Button value="Delete" handleClick={deleteLetter} />
  <button>Shuffle Letters</button>
  <button>Enter</button>
</section>
