<article>
  <div class="todo">
    <div class="ctr">
      <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-confetti" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
        <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
        <path d="M4 5h2" />
        <path d="M5 4v2" />
        <path d="M11.5 4l-.5 2" />
        <path d="M18 5h2" />
        <path d="M19 4v2" />
        <path d="M15 9l-1 1" />
        <path d="M18 13l2 -.5" />
        <path d="M18 19h2" />
        <path d="M19 18v2" />
        <path d="M14 16.518l-6.518 -6.518l-4.39 9.58a1 1 0 0 0 1.329 1.329l9.579 -4.39z" />
      </svg>
      <h2>SVINĒT SVĒTKUS</h2>
    </div>
    <p>Ruckas muiža piedāvā svinēt kā mazus, tā lielus svētkus! Sākot ar dzimšanas dienam, beidzot ar kāzām.</p>
  </div>
    
</article>

<style>
  article {
    width: 100vw;
    min-height: 100vh;
    background-image: linear-gradient(to bottom, var(--black-transparent), transparent),url("https://rucka.vercel.app/103A2674.webp");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    position: relative;
  }

  .ctr {
    display: flex;
    align-items: center;
    flex-direction: column;
    gap:10px;
  }

  h2 {
    font-size: 2.5rem;
    font-family: var(--accent-font);
    color: var(--black);
    text-align: center;
    margin-bottom: 30px;
  }

  .todo {
    width: 400px;
    height: 600px;
    max-width: 90vw;
    background: linear-gradient(var(--white) 60%, transparent);
    transform: translateX(10vw) translateY(20vh);
    padding: 20px;

    box-shadow: 0px -10px 20px rgba(0,0,0,0.4);

  }

  svg {
    color: var(--avenu-sarkana);
  }

  p {
    color: var(--black);
    font-size: 1.1rem;
  }
</style>