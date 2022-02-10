<script>
   let someText = `Frontend Developer AdMech`; 
   let count = 0;
    let style = { darkMode: false };
   function addCount(){
      count++;
   }
   function toggleMode() {
      style.darkMode = !style.darkMode;
      window.document.body.classList.toggle('dark-mode');
   }
</script>

<style>

</style>

<div class="About">
  {#if !style.darkMode}
    <p>
      <span>Hello LigthMode</span>
    </p>
  {:else}
      <p><span>Hello darkMode</span>
    </p>
  {/if}
  <button on:click={addCount}>Click {count === 0 ? '' : count}</button>
  <button on:click={toggleMode}>DarkMode</button>
</div>