<script>
  let numbers = [1, 2, 3, 4];

  function addNumber() {
    // numbers.push(numbers.length + 1);
    // needs a redundant assignment because
		// svelte reactivity is triggered by assignments
    // numbers = numbers;

    // more "idiomatic" solution:
    numbers = [...numbers, numbers.length + 1];
  }

  $: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}>
  Add a number
</button>
