<script>
  export let letter = '';
  export let handleClick;
</script>

<style>
  button {
    background-color: transparent;
    outline: none;
    border: none;
  }
  svg.hive-cell.outer {
  }
  polygon.cell-fill {
    fill: hsl(0, 0%, 90%);
  }
  text.cell-letter {
    text-transform: uppercase;
  }
</style>

<button on:click={e => handleClick(e, letter)}>
  <svg class="hive-cell outer" viewBox="0 0 120 103.92304845413263">
    <polygon
      class="cell-fill"
      points="0,51.96152422706631 30,0 90,0 120,51.96152422706631 90,103.92304845413263
      30,103.92304845413263"
      stroke="white"
      stroke-width="7.5" />
    <text class="cell-letter" x="50%" y="50%" dy="10.75%">{letter}</text>
  </svg>
</button>
