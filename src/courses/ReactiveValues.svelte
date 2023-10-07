<script>
  let firstName = "Faid";
  let lastName = "Fadjri";

  // Reactive Values -- Wacthing of variable changes
  $: fullName = `${firstName} ${lastName}`;

  // Reactive Statement == Watching of variable changes but instead of value it run a statement
  $: {
    console.log("Your first name was : " + firstName);
  }

  const onReactiveStatementTriggered = () => {};
</script>

<main>
  <h1>{fullName}</h1>

  <input type="text" bind:value={firstName} />
  <input type="text" bind:value={lastName} />
</main>

<style>
  input {
    padding: 10px 20px;
  }
</style>
