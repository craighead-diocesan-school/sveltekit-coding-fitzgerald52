<script>
  let welcomeMessage = ''
  function sayHi() {
    welcomeMessage = 'Hi!'
  }
</script>

<main>
  <p>{welcomeMessage}</p>
  <button on:click={sayHi}> press me </button>
</main>

<style>
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
