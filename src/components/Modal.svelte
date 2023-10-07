<script>
  // to make it as prop wrapper
  export let show = false;
</script>

<main>
  {#if show}
    <p>Hello Fellas</p>
    <button>SIGN UP FOR FREE</button>
  {/if}
</main>
