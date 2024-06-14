<script>
  let imageUrl = 'https://picsum.photos/200'
  let caption = 'example image '
  let linkUrl = 'google.com'
</script>

<figure>
  <a><img src={imageUrl} alt="" href={linkUrl} /></a>
  <figcaption><p>{caption}</p></figcaption>
</figure>

<style>
  figure {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
    padding: 1.5rem;
    width: fit-content;
    border-radius: 10px;
    box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
    backdrop-filter: blur(4px);
    background: rgba(98, 217, 255, 0.25);
  }
</style>
