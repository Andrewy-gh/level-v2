<section class="container flex">
  <div>
    <img src="https://placehold.co/300x200" alt="placeholder" />
    <h3>Lorem ipsum dolor sit amet.</h3>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
      veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
      commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
      velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
      cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
      est laborum.
    </p>
  </div>
  <div>
    <img src="https://placehold.co/300x200" alt="placeholder" />
    <h3>Lorem ipsum dolor sit amet.</h3>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
      veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
      commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
      velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
      cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id
      est laborum.
    </p>
  </div>
</section>

<style>
  img {
    display: block;
  }
  .container {
    width: min(1280px, 100% - 2rem);
    margin-inline: auto;
    display: flex;
    gap: 1rem;
    flex-direction: column;
    @media only screen and (min-width: 900px) {
      flex-direction: row;
    }
  }

  .container > div {
    display: flex;
    flex-direction: column;
    flex-grow: 0;
  }
</style>
