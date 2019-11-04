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
    currentWord += letter;
  };

  const deleteLetter = () => {
    console.log('delete letter');
    const newWord = currentWord.slice(0, -1);
    currentWord = newWord;
  };

  const handleKeydown = e => {
    console.log(e);
    if (letters.includes(e.key)) {
      console.log('this is a hive letter');
    } else {
      console.log('This is NOT a hive letter');
    }
  };
</script>

<style>
  section.hive {
    position: relative;
  }
  form .hidden {
    visibility: collapse;
  }
  form input[type='text'] {
    text-align: center;
  }
</style>

<svelte:body on:keydown={handleKeydown} />
<section>
  <form on:submit={handleSubmit}>
    <input type="text" name="word" id="word" bind:value={currentWord} value={currentWord} />
    <input type="submit" id="submit-form" class="hidden" />
  </form>
  <section class="hive">
    {#each letters as letter, i}
      <Cell handleClick={addLetter} {letter} center={i === letters.length - 1} />
    {/each}
  </section>
  <Button value="Delete" handleClick={deleteLetter} />
  <button>Shuffle Letters</button>
  <label for="submit-form" tabindex="0">Enter</label>
</section>
