<script>
  import Modal from "./components/Modal.svelte";

  let show = false;
  const onButton = () => {
    show = !show;
  };
</script>

<Modal {show} />
<main>
  <br />
  <button on:click={onButton}>Show / Hide Modal</button>
</main>
