<script>
  import Props from "./Props.svelte";

  let isModalShow = false;
  const toggleModal = () => {
    isModalShow = !isModalShow;
  };
</script>

<!-- Event Forwarding -->
<!-- a callback function access from the parent component to the child component -->
<Props show={isModalShow} on:click={toggleModal} />
