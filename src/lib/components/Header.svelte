<header>
  <div class="bt-10">
    <nav>
      <a href="/"><img src="/logo.png" alt="Logo"/></a>
      <ul>
        <li><a href="/">PAR MUIŽU</a></li>
        <li><a href="/">AFIŠA</a></li>
        <li><a href="/">IZKLAIDE</a></li>
        <li><a href="/">NAKŠŅOŠANA</a></li>
        <li><a href="/">BLOGS</a></li>
        <li><a href="/">GALERIJA</a></li>
      </ul>
    </nav>
  </div>
</header>

<style>
  header {
    position: fixed;
    top:0;
    left: 0;
    width: 100vw;
    z-index: 1000;

    background: linear-gradient(to bottom, var(--black-transparent) 10% , transparent);

    /* backdrop-filter: blur(0.5px); */
  }

  .bt-10 {
    width: 100%;
    height: 100%;
    border-top: 10px solid var(--avenu-sarkana);
  }

  nav {
    max-width: 1100px;
    margin: 0 auto;
    display: flex;
    gap: 30px;
  }

  img {
    width: 140px;
    transform: translateY(-1px);
  }

  ul {
    display: flex;
    gap: 40px;
    align-items: center;
    padding-bottom: 40px;
  }

  li {
    list-style-type: none;

  }

  a {
    text-decoration: none;
    color: var(--white);
    font-size: 1.2rem;

  }
</style>