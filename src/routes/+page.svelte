<script>
  let name = 'world '
  let imageUrl = 'https://picsum.photos/200'
  import ImageCard from '../lib/ImageCard.svelte'
  import HiButton from '../lib/HiButton.svelte'
  import Converter from '../lib/Converter.svelte'
  let isChecked = false
  let selectedOption = 'Option 1'
  let count = 0

  function increment() {
    count = count + 1
  }
  function decrement() {
    count = count - 1
  }
</script>

<main>
  <ImageCard />

  <input bind:value={name} placeholder="Enter your name" />
  <p>hello {name}!</p>

  <input type="checkbox" bind:checked={isChecked} />

  <p>The checkbox is {isChecked}.</p>
  <select bind:value={selectedOption}>
    <option value="Option 1">Option 1</option>
    <option value="Option 2">Option 2</option>
    <option value="Option 3">Option 3</option>
  </select>

  <p>You selected: {selectedOption}</p>
  <p>Count: {count}</p>
  <button on:click={increment}>up</button>
  <button on:click={decrement}>down</button>

  <HiButton />
  <Converter />
</main>

<footer>
  <p>&copy; Craighead Diocesan School 2024</p>
</footer>

<style>
  main {
    background-image: url(aditya-chinchure.jpg);
  }
  p {
    color: aliceblue;
  }
</style>
