<script>
  import TitleBar from './components/TitleBar.svelte';
  import MenuBar from './components/MenuBar.svelte';
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
