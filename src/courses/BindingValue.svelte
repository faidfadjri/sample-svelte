<script>
  let color = "black";
  const onButtonClickEvent = () => {
    alert("Button clicked");
  };

  const onInputChangeEvent = (e) => {
    const { value } = e.target;
    color = value;
  };
</script>

<main>
  <h1>Your Color : {color}</h1>
  <p>Welcome to svelte development</p>

  <p style="color: {color};">Color : {color}</p>
  <!-- On Input Changes -->
  <!-- <input type="text" on:input={onInputChangeEvent} value={color} /> -->
  <!-- Bind Input (it will automatically update the variable and set the value)  -->

  <input type="text" bind:value={color} />
  <button on:click={onButtonClickEvent} value={color}>Click Me</button>
</main>

<style>
  input {
    padding: 10px 20px;
  }
</style>
