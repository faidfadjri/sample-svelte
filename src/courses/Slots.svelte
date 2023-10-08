<!-- Slots -->
<!-- How to send the HTML code to the child as a children element inside of it -->

<script>
  export let show = false;
</script>

{#if show}
  <!-- svelte-ignore a11y-click-events-have-key-events -->
  <!-- svelte-ignore a11y-no-static-element-interactions -->

  <!-- make on:click:self to make the handler is only fires when the target (actual target) are clicked -->
  <div class="backdrop" on:click|self>
    <div class="modal">
      <slot />
      <slot name="spesific-slot" />
    </div>
  </div>
{/if}
<button on:click>Show Modal</button>

<style>
  .backdrop {
    height: 100vh;
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background-color: rgba(0, 0, 0, 0.2);
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .modal {
    background-color: white;
    width: fit-content;
    padding: 50px;
    border-radius: 10px;
  }
</style>
