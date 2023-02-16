<style>
  header {
    background: #136c72;
    padding: 1em 0;
    text-align: center;
  }

  .nav {
    visibility: hidden;
    height: 0;
    position: absolute;
  }

  .nav.open {
    visibility: visible;
    height: auto;
    position: relative;
  }

  .nav__list {
    margin: 0;
    padding: 1rem 0;
    list-style: none;
    font-size: .9rem;
  }

  .nav__item {
    margin-top: 1rem;
  }

  .nav__link {
    color: #fff;
    text-decoration: none;
    text-transform: uppercase;
  }

  .nav__link--button {
    background: #fff;
    color: #136c72;
    padding: .25em 1em;
    border-radius: 10em;
  }

  .nav__link:hover,
  .nav__link:focus {
    opacity: .75;
  }

  .nav__toggle {
    cursor: pointer;
    border: 0;
    width: 3rem;
    height: 3rem;
    padding: 1em;
    border-radius: 50%;
    background: #072a2d;
    color: white;
    transition: opacity 250ms ease;
    position: absolute;
    left: 0;
  }

  .nav-toggle:focus,
  .nav-toggle:hover {
    opacity: 0.75;
  }

  .hamburger,
  .hamburger::before,
  .hamburger::after {
    display: block;
    margin: 0 auto;
    height: 3px;
    background: white;
  }

  .hamburger::before,
  .hamburger::after {
    content: "";
    width: 100%;
  }

  .hamburger::before {
    transform: translateY(-6px);
  }

  .hamburger::after {
    transform: translateY(3px);
  }
    
  .logo {
    height: 30px;
  }

  @media (min-width: 800px) {
  .nav-toggle {
      display: none;
  }

  .nav {
    visibility: visible;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    position: relative;
    height: auto;
  }

  .nav__list {
    display: flex;
    margin: 0;
    list-style: none;
  }

  .nav__list--primary {
    margin: 0 auto;
  }

  .nav__item {
    margin: 0 0 0 1.5em;
  }

  .row {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>

<script>
  let isMenuOpen = false;
  function toggleMenu(){
    isMenuOpen = !isMenuOpen
  }
</script>

<header>
    <div class="container row">
      <button 
        class="nav__toggle"
        on:click={toggleMenu}
        aria-label="open navigation">
        <span class="hamburger"></span>
      </button>
      <a class="logo" href="/">
        <img src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/308367/logo.svg" alt="">
      </a>
      <nav 
      class:nav={isMenuOpen}
      >
        <ul class="nav__list nav__list--primary">
          <li class="nav__item"><a href="/" class="nav__link">Home</a></li>
          <li class="nav__item"><a href="/about" class="nav__link">About</a></li>
          <li class="nav__item"><a href="/work" class="nav__link">Work</a></li>
          <li class="nav__item"><a href="/posts" class="nav__link">Blog</a></li>
          <li class="nav__item"><a href="/contact" class="nav__link nav__link--button">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>
 
  <slot></slot>