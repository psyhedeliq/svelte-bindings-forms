<script>
  let val = "Maracana";

  $: console.log(val);

  const setValue = event => {
    val = event.target.value;
  };
</script>

<!-- <input type="text" value={val} on:input={setValue} /> -->
<input type="text" bind:value={val} />
