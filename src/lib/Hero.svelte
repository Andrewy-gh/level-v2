<div class="container">
  <img
    class="image"
    src="https://images.unsplash.com/photo-1563305589-3c582d447a99?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2061&q=80"
    alt="pizza shop"
  />
  <div class="text">
    <h1>Content Testing</h1>
    <p class="container-narrow">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua.
    </p>
    <button>Button here</button>
  </div>
</div>

<style>
  .container {
    width: min(1280px, 100% - 2rem);
    margin-inline: auto;
    text-align: center;
    display: grid;
    place-items: center;
  }

  .container > * {
    grid-row: 1 /-1;
    grid-column: 1/ -1;
  }

  .container-narrow {
    width: min(40ch, 100% - 2rem);
    margin-inline: auto;
  }

  img {
    display: block;
    max-width: 100%;
  }

  .text {
    color: white;
  }

  @media only screen and (min-width: 800px) {
    .container {
      grid-template-columns: 1fr, 1fr;
    }
    .text {
      color: black;
      grid-column: 1;
    }
    .image {
      grid-column: 2;
    }
  }
</style>
