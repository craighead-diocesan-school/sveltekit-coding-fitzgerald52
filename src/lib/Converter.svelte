<script>
  let USD = ''
  USD = Number(USD)
  let NZD = ''
  NZD = Number(NZD)
  const convrate = 1.63
  // button that changes value from input using maths
  function changer() {
    NZD = convrate * USD
  }
</script>

<main>
  <label for="USD">
    <!-- links the input the the variable  -->
    <input bind:value={USD} placeholder="Enter USD " />
  </label>
  <!-- completes the function when the button is clicked  -->
  <button on:click={changer}> convert </button>
  <p>{NZD}</p>
</main>

<style>
  /* styles the buttons  */
  button {
    width: 10rem;
    height: 10rem;
    margin: 3rem 3rem;
    border: none;
    border-radius: 50px;
    background: linear-gradient(145deg, #cacaca, #f0f0f0);
    box-shadow:
      10px 10px 30px #bebebe,
      -10px -10px 30px #ffffff;
  }

  button:active {
    box-shadow:
      inset 20px 20px 60px #bebebe,
      inset -20px -20px 60px #ffffff;
  }

  p {
    color: #ffffff;
  }
</style>
