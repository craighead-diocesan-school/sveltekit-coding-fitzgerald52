<script>
  let role = ''
</script>

<main>
  <!-- allows users to input their roll -->
  <p>Please enter your roll of either admin, user, editor, or guest</p>
  <input bind:value={role} placeholder="enter your role " />
  <!-- puts out different messagges based on what the user inputs -->
  {#if role == 'admin'}
    <h1>Welcome admin. you have full access to the server</h1>
  {:else if role == 'user'}
    <h1>welcome user. your access is limited</h1>
  {:else if role == 'editor'}
    <h1>you can edit content but still have limited access</h1>
  {:else if role == 'guest'}
    <h1>you have veiw-only access</h1>
  {:else}
    <h1>please enter valid role</h1>
  {/if}

  <style>
    h1 {
      color: aliceblue;
    }
    p {
      color: aliceblue;
    }
  </style>
</main>
