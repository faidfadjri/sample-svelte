<script>
  let firstName;
  let LastName;

  const onSubmit = () => {
    console.log("FirstName : " + firstName);
    console.log("FirstName : " + LastName);
  };
</script>

<form on:submit|preventDefault={onSubmit}>
  <input type="text" placeholder="firstName" bind:value={firstName} />
  <input type="text" placeholder="LastName" bind:value={LastName} />
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
</style>
