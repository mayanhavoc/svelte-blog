<script>
  import About from './about/+page.svelte';
  import Work from './work/+page.svelte';
</script>

<svelte:head>
    <title>Home</title>
</svelte:head>

<style>
:global(body){
    margin: 0;
    font-family: "Roboto", sans-serif;
    font-size: 1.3125rem;
    line-height: 1.6; 
}

:global(.container){
    width: 80%;
    max-width: 1100px;
    margin: 0 auto;
    /* added for nav-toggle positioning */
    position: relative;
}
:global(*, *::before, *::after){
    box-sizing: border-box;
}
:global(img){
    max-width: 100%;
}
:global(a){
    text-decoration: none;
    color: #fff;
}

:global(.btn) {
  display: inline-block;
  text-decoration: none;
  text-transform: uppercase;
  color: #23424a;
  font-weight: 900;
  background-color: #38cfd9;
  padding: 0.75em 2em;
  border-radius: 100px;
}

:global(
  .btn:hover,
  .btn:focus
  ) {
  opacity: 0.75;
}

h1 {
  font-size: 3rem;
  margin-top: 0;
}

section {
  padding: 4em 0;
}

.hero {
  padding: 100px 0;
  background-color: #23424a;
  color: #fff;
}

.hero__text {
  width: 62%;
}

.hero__img {
  margin-top: 2em;
}

.hero p {
  margin-bottom: 3em;
}
</style>

<section class="hero">
  <div class="container row">
    <div class="hero__text">  
      <h1>Full stack web3 and smart contract development</h1>
      <a href="#" class="btn">Contact</a>
    </div>
  </div>
</section>
<About />
<Work />
    

