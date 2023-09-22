<script>
  import Nav from './lib/Nav.svelte';
  import Hero from './lib/Hero.svelte';
  import CallToAction from './lib/CallToAction.svelte';
  import Featured from './lib/Featured.svelte';
  import CallToAction2 from './lib/CallToAction2.svelte';
  import Footer from './lib/Footer.svelte';
</script>

<main class="flow">
  <Nav />
  <Hero />
  <CallToAction />
  <Featured />
  <CallToAction2 />
  <Footer />
</main>
<div class="flow">
  <div>Item 1</div>
  <div class="red">Item 2</div>
  <div class="mt-1">Item 3</div>
</div>

<style>
  .flow > *:where(:not(:first-child)) {
    margin-top: 1rem;
    outline: 1px solid red;
  }
  .red {
    color: red;
  }
  .mt-1 {
    margin-top: 2rem;
  }
</style>
