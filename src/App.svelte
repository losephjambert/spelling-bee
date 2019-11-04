<script>
  import TitleBar from './components/TitleBar.svelte';
  import MenuBar from './components/MenuBar.svelte';
  import Hive from './components/Hive.svelte';
  export let title;
</script>

<style>
  h1 {
    color: #f8cd05;
  }
</style>

<header>
  <TitleBar />
  <MenuBar />
</header>
<main>
  <Hive />
</main>
