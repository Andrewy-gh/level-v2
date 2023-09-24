<script>
  const content = [
    {
      image: 'https://placehold.co/300x200',
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris aliquip ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia mollit anim id est laborum.',
      title: 'Lorem ipsum dolor sit amet.',
    },
    {
      image: 'https://placehold.co/300x200',
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris aliquip ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia mollit anim id est laborum.',
      title: 'Lorem ipsum dolor sit amet.',
    },
    {
      image: 'https://placehold.co/300x200',
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris aliquip ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia mollit anim id est laborum.',
      title: 'Lorem ipsum dolor sit amet.',
    },
    {
      image: 'https://placehold.co/300x200',
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris aliquip ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia mollit anim id est laborum.',
      title: 'Lorem ipsum dolor sit amet.',
    },
    {
      image: 'https://placehold.co/300x200',
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris aliquip ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia mollit anim id est laborum.',
      title: 'Lorem ipsum dolor sit amet.',
    },
    {
      image: 'https://placehold.co/300x200',
      text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris aliquip ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia mollit anim id est laborum.',
      title: 'Lorem ipsum dolor sit amet.',
    },
  ];
</script>

<div class="alternating-container">
  {#each content as item, index}
    <div
      class="alternating-item {index % 2 === 0
        ? 'image-on-right'
        : 'image-on-left'}"
    >
      <div class="image">
        <img src={item.image} alt={`Image ${index}`} />
      </div>
      <div class="text">
        <h2>{item.title}</h2>
        <p>{item.text}</p>
      </div>
    </div>
  {/each}
</div>

<style>
  .alternating-container {
    width: min(1280px, 100% - 2rem);
    margin-inline: auto;
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }
  .alternating-item {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  @media only screen and (min-width: 800px) {
    .alternating-item {
      flex-direction: row;
      gap: 2rem;
    }
    .image-on-right .image {
      order: 2;
    }
    .image-on-left .text {
      order: 2;
    }
  }
</style>
