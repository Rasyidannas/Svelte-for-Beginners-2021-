<script>
  let count = 0;

  function increment () {
    count ++;
  }
</script>

<main class="flex flex-col justify-center items-center h-screen space-y-4">
  {count}
  <button on:click={increment} class="btn">Button</button>
</main>

<style>

</style>
