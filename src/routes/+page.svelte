<script>
  //  imports from other pages
  import ImageCard from '../lib/ImageCard.svelte'
  import HiButton from '../lib/HiButton.svelte'
  import Converter from '../lib/Converter.svelte'
  import Ifstate from '../lib/Ifstate.svelte'
  import UserRole from '../lib/UserRole.svelte'
  // defines variables
  let isChecked = false
  let selectedOption = 'Option 1'
  let name = 'world '
  let count = 0
  // increases and decreases by 1
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
  <!-- checkbox -->
  <input type="checkbox" bind:checked={isChecked} />
  <p>The checkbox is {isChecked}.</p>

  <!-- allows the users to select an optoion -->
  <select bind:value={selectedOption}>
    <option value="Option 1">Option 1</option>
    <option value="Option 2">Option 2</option>
    <option value="Option 3">Option 3</option>
  </select>
  <p>You selected: {selectedOption}</p>

  <!-- counts up and down -->
  <p>Count: {count}</p>
  <button on:click={increment}>up</button>
  <button on:click={decrement}>down</button>

  <HiButton />
  <Converter />
  <Ifstate />
  <UserRole />
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
