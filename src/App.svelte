<script>
  let active = 1;

  function changeActive(num) {
    active = num;
  }
</script>

<main class="flex flex-col justify-center items-center h-screen space-y-4">
  <div class="join">
    <button 
      on:click={() => changeActive(1)} 
      class="btn join-item {active === 1 ? "btn-active" : ""}"
      >Button</button>
    <button 
      on:click={() => changeActive(2)} 
      class="btn join-item {active === 2 ? "btn-active" : ""}"
      >Button</button>
    <button 
      on:click={() => changeActive(3)} 
      class="btn join-item {active === 3 ? "btn-active" : ""}"
      >Button</button>
  </div>
</main>

<style>

</style>
