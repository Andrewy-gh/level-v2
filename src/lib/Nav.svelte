<script>
  import Hamburger from '../assets/Hamburger.svelte';
  import Xmark from '../assets/Xmark.svelte';

  let open = false;

  function toggleOpen() {
    open = !open;
  }
</script>

<nav>
  <div on:click={toggleOpen} class="hamburger">
    {#if open}
      <Xmark />
    {:else}
      <Hamburger />
    {/if}
  </div>
  <div>
    <a href="">CLASSES</a>
    <a href="">HIRE US</a>
  </div>
  <div>Logo</div>
  <div>
    <a href="">HIRE US</a>
  </div>
</nav>
<div class="menu-container">
  {#if open}
    <ul class="menu" class:open class:close={!open}>
      <li><a href="#">Item 1</a></li>
      <li><a href="#">Item 2</a></li>
      <li><a href="#">Item 3</a></li>
    </ul>
  {/if}
</div>

<style>
  nav {
    width: min(1280px, 100% - 2rem);
    margin-inline: auto;
    display: flex;
    justify-content: space-between;
    gap: 1rem;
  }
  @media only screen and (min-width: 800px) {
    .hamburger {
      display: none;
    }
  }

  .menu-container {
    position: relative;
  }

  @keyframes slideDown {
    0% {
      max-height: 0;
    }
    100% {
      max-height: 500px;
    }
  }

  @keyframes slideUp {
    0% {
      max-height: 500px;
    }
    100% {
      max-height: 0;
    }
  }

  .menu {
    max-height: 0;
    width: 100%;
    overflow: hidden;
    position: absolute;
    top: 0;
    background-color: grey;
    color: white;
    padding: 1rem;
  }

  .menu.open {
    animation: slideDown 0.5s ease-in-out forwards;
  }

  .menu.close {
    animation: slideUp 0.5s ease-in-out forwards;
  }
</style>
