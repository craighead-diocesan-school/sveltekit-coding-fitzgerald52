<script>
  let name = 'Bob'
</script>

{#if name}
  <h1>Hello, {name}!</h1>
{:else}
  <h1>Hello, stranger!</h1>
{/if}
{#if name == 'Alice'}
  <h1>Welcome back, Alice!</h1>
{:else if name == 'Bob'}
  <h1>Not you again!</h1>
{:else}
  <h1>Hello, {name}!</h1>
{/if}

<style>
  h1 {
    color: aliceblue;
  }
</style>
