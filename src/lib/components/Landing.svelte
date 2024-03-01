<article>
  <div class="centered">
    <p class="lead">Laipni lūgti</p>
    <h1>RUCKAS MUIŽĀ</h1>
  </div>
  <div class="scrool">
    <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-arrow-down" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#ffffff" fill="none" stroke-linecap="round" stroke-linejoin="round">
      <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
      <path d="M12 5l0 14" />
      <path d="M18 13l-6 6" />
      <path d="M6 13l6 6" />
    </svg>
  </div>
</article>

<style>
  article {
    width: 100vw;
    height: 100vh;
    background-image: linear-gradient(to bottom, var(--black-transparent), transparent),url("background.webp");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
  }

  h1 {
    font-size: 6rem;
    font-family: var(--accent-font);
    color: var(--white);
  }

  .lead {
    font-size: 2rem;
    text-align: center;
    color: var(--white);
    letter-spacing: 0.15rem;
  }

  .centered {
    margin-bottom: 100px;
  }

  .scrool {
    position: absolute;
    bottom: 30px;
    left: 50%;
    transform: translateX(-50%);
    width: 60px;
    height: 60px;
    background-color: var(--avenu-sarkana);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

</style>