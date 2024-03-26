<script>
  let number = 1;

  function add5() {
    number += 5;
  }

  // This is a reactive variable
  $: multiple = number * 2;
</script>

<main class="flex flex-col justify-center items-center h-screen space-y-4">
  <p>The number is: {number}</p>
  <button class="btn-primary" on:click={add5}>Add Five</button>

  <p>The number multipled by 2 is {multiple}</p>
</main>

<style>

</style>
