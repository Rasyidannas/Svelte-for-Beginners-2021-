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

  {#if multiple < 50}
  <div role="alert" class="alert alert-success">
    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" class="stroke-info shrink-0 w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
    <span>Numbers look good!</span>
  </div>
  {:else}
  <div role="alert" class="alert alert-error">
    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" class="stroke-info shrink-0 w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
    <span>Numbers are to high!</span>
  </div>
  {/if}
</main>

<style>

</style>
