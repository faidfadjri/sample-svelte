<script>
  // Type of event modifier
  // once - makes sure the event can only fire once (removes handler)
  // preventDefault - prevent the default action (e.g e.preventDefault)
  // self - only fires the event if the clicked element is the target
  import EventModifierModal from "../components/EventModifierModal.svelte";

  let show = false;

  const toggleModal = () => {
    show = !show;
  };
</script>

<EventModifierModal on:click={toggleModal} {show} message="This is my Modal" />
