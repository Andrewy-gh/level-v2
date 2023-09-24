<script>
  import Nav from './lib/Nav.svelte';
  import Hero from './lib/Hero.svelte';
  import CallToAction from './lib/CallToAction.svelte';
  import Featured from './lib/Featured.svelte';
  import CallToAction2 from './lib/CallToAction2.svelte';
  import Footer from './lib/Footer.svelte';
</script>

<main class="flow">
  <div>
    <Nav />
  </div>
  <div>
    <Hero />
  </div>
  <div>
    <CallToAction />
  </div>
  <div>
    <Featured />
  </div>
  <div>
    <CallToAction2 />
  </div>
  <div>
    <Footer />
  </div>
</main>

<style>
  .flow > *:where(:not(:first-child)) {
    margin-top: 3rem;
    outline: 1px solid red;
  }
</style>
