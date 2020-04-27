<script>
  import CustomInput from "./CustomInput.svelte";
  import Toggle from "./Toggle.svelte";

  let val = "Maracana";
  let selectedOption = 1;
  let price = 0;
  let agreed;
  // let favColor = "green";
  let favColor = ["green"];

  $: console.log(val);
  $: console.log(selectedOption);
  $: console.log(price);
  $: console.log(agreed);
  $: console.log(favColor);

  const setValue = event => {
    val = event.target.value;
  };
</script>

<!-- <input type="text" value={val} on:input={setValue} /> -->
<!-- <input type="text" bind:value={val} /> -->
<CustomInput bind:val />
<Toggle bind:chosenOption={selectedOption} />

<!-- this will always return a stri ng even if the type is number because this is the default behavior in the DOM and JS -->
<!-- <input
  type="number"
  value={price}
  on:input={event => console.log(event.target.value)} /> -->

<!-- Svelte actualy helps you with conversion if you use the two-way binding  bind directive -->
<input type="number" bind:value={price} />

<label>
  <input type="checkbox" bind:checked={agreed} />
  Agree to terms?
</label>

<h1>Favorite color?</h1>
<!-- <label>
  <input type="radio" name="color" value="red" bind:group={favColor} />
  Red
</label>
<label>
  <input type="radio" name="color" value="green" bind:group={favColor} />
  Green
</label>
<label>
  <input type="radio" name="color" value="blue" bind:group={favColor} />
  Blue
</label> -->

<label>
  <input type="checkbox" name="color" value="red" bind:group={favColor} />
  Red
</label>
<label>
  <input type="checkbox" name="color" value="green" bind:group={favColor} />
  Green
</label>
<label>
  <input type="checkbox" name="color" value="blue" bind:group={favColor} />
  Blue
</label>
