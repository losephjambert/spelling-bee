<script>
  import Button from './Button.svelte';

  const saveProgress = e => {
    console.log(e.target, 'Save Progress');
  };

  const showHelp = e => {
    console.log(e.target, 'Show Help');
  };
</script>

<style>
  section {
    border-top: 1px solid grey;
    border-bottom: 1px solid grey;
    padding: 24px;
    padding-left: 32px;
    padding-right: 32px;
  }
</style>

<section>
  <Button value="Help" handleClick={showHelp} />
  <Button value="Save" handleClick={saveProgress} />
</section>
