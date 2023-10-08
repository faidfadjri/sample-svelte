<script>
  import Slots from "./Slots.svelte";
  let show = false;

  const toggleModal = () => {
    show = !show;
  };
</script>

<!-- if the state are same just using {show} -->
<Slots {show} on:click={toggleModal}>
  <p>This is the HTML code from the parent</p>

  <p slot="spesific-slot">This is a spesific slot defined</p>
</Slots>
