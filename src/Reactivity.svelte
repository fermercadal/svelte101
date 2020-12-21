<script>
  let count = 0;
  let label = '<strong>Happy</strong> landings: ';

  $: doubled = count * 2;
  $: {
    console.log(`the count is ${count}`);
    console.log(`So uncivilised`);
  }

  function handleClick() {
    count += 1;
  }
</script>

<section>
  <button on:click={handleClick}>Another happy landing</button>
  
  <p>{@html label} {count} {count === 1 ? 'time' : 'times'}</p>
  <p>..doubled is {doubled}</p>
</section>

