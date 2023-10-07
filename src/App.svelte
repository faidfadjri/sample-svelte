<script>
  let people = [
    { name: "Jimmy", color: "black", id: 1 },
    { name: "Harun", color: "orange", id: 2 },
    { name: "Michael", color: "purple", id: 3 },
  ];

  const onDelete = (person) => {
    people = people.filter((current) => current.id != person.id);
  };
</script>

<main>
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
