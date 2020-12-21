<script>
  export let name;

  let who = 'there';
  const obk = {
    who: 'He',
    name: 'Obi-Wan Kenobi',
    title: 'Jedi Master',
    how: 'civilised'
  }

  import Nested from './Nested.svelte';
  import Nested2 from './Nested2.svelte';
  import Reactivity from './Reactivity.svelte';
  import ArrayObject from './ArrayObject.svelte';
</script>

<main>
  <h1>Hello {who}</h1>
  <p>{name} Following <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>

  <Nested/>

  <Reactivity/>

  <ArrayObject/>

  <Nested2 answer={42} {...obk}/>
  <Nested2/>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>