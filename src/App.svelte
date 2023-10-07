<script>
  let people = [
    { name: "Jimmy", color: "black", id: 1 },
    { name: "Harun", color: "orange", id: 2 },
    { name: "Michael", color: "purple", id: 3 },
  ];

  const onDelete = (person) => {
    people = people.filter((current) => current.id != person.id);
  };

  let num = 28;
</script>

<main>
  <!-- Conditional Statement -->

  {#if num > 20}
    <p>greater than 20</p>
  {:else if num > 5}
    <p>greater than 5</p>
  {/if}

  <!-- each refer to map on react & (person.id) refer to keys on react -->
  {#each people as person (person.id)}
    <div>
      <h3>Name : {person?.name}</h3>
      <h4>Color : {person?.color}</h4>
      <button on:click={() => onDelete(person)}>delete</button>
    </div>
  {:else}
    <p>There is no record of the data</p>
  {/each}
</main>
