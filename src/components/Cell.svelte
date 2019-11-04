<script>
  export let letter = '';
  export let handleClick;
  export let center;
</script>

<style>
  svg.hive-cell {
    width: 75px;
  }
  svg.hive-cell.center > polygon.cell-fill {
    fill: #f8cd05;
  }
  polygon.cell-fill {
    fill: #e6e6e6;
  }
  text.cell-letter {
    text-transform: uppercase;
    text-anchor: middle;
    font-size: 2rem;
  }
</style>

<svg
  class="hive-cell {center ? 'center' : 'outer'}"
  viewBox="0 0 120 103.92304845413263"
  on:click={e => handleClick(e, letter)}>
  <polygon
    class="cell-fill"
    points="0,51.96152422706631 30,0 90,0 120,51.96152422706631 90,103.92304845413263
    30,103.92304845413263"
    stroke="white"
    stroke-width="7.5" />
  <text class="cell-letter" x="50%" y="50%" dy="10.75%">{letter}</text>
</svg>
