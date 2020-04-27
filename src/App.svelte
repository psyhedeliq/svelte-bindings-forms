<script>
  import CustomInput from "./CustomInput.svelte";
  import Toggle from "./Toggle.svelte";

  let val = "Maracana";
  let selectedOption = 1;

  $: console.log(val);
  $: console.log(selectedOption);

  const setValue = event => {
    val = event.target.value;
  };
</script>

<!-- <input type="text" value={val} on:input={setValue} /> -->
<!-- <input type="text" bind:value={val} /> -->
<CustomInput bind:val />
<Toggle bind:chosenOption={selectedOption} />
