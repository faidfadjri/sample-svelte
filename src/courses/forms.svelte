<!-- Bind Groups used for the input value which have the same function -->

<script>
  let firstName;
  let LastName;

  let skills = [];

  const onSubmit = () => {
    console.log("FirstName : " + firstName);
    console.log("FirstName : " + LastName);
    console.table(skills);
  };
</script>

<form on:submit|preventDefault={onSubmit}>
  <input type="text" placeholder="firstName" bind:value={firstName} />
  <input type="text" placeholder="LastName" bind:value={LastName} />

  <p>Your Skills</p>
  <ul>
    <li>
      <label for="Fighting" class="checkboxes">
        <input
          id="Fighting"
          type="checkbox"
          bind:group={skills}
          value="Fighting"
        />
        Fighting
      </label>
    </li>
    <li>
      <label for="Programming" class="checkboxes">
        <input
          id="Programming"
          type="checkbox"
          bind:group={skills}
          value="Programming"
        />
        Programming
      </label>
    </li>
    <li>
      <label for="Arts" class="checkboxes">
        <input id="Arts" type="checkbox" bind:group={skills} value="Arts" />
        Arts
      </label>
    </li>
  </ul>
  <button>Submit</button>
</form>

<style>
  form {
    display: flex;
    flex-direction: column;
    row-gap: 10px;
  }

  input {
    padding: 10px;
  }

  ul {
    list-style: none;
    padding: 0px;
    display: flex;
    flex-direction: column;
    align-items: self-start;
    gap: 10px;
  }

  li {
    padding: 0px;
  }
</style>
