<script>
  let num = 28;
</script>

<main>
  <!-- Conditional Statement -->
  {#if num > 20}
    <p>greater than 20</p>
  {:else if num > 5}
    <p>greater than 5</p>
  {/if}
</main>
