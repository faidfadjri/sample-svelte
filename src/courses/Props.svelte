<script>
  import Modal from "../components/Modal.svelte";

  export let show = false;
</script>

<Modal {show} />
<main>
  <br />

  <!-- Pass the empty on:click to make the button is expose to the parent -->
  <button on:click>Show / Hide Modal</button>
</main>
