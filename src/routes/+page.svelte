<script>
  import events from "$lib/data/events.json";
  import Date from "./Date.svelte";

</script>

<main>
  <img src="logo.png" alt="Ruckas muiža" id="logo"/>
  <div class="inner-content">
    <div class="header-distributer">
      <h1>RUCKAS MUIŽA piedāvā</h1>
      <h2>2023. gada DECEMBRA <strong>PASĀKUMU KALENDĀRS</strong></h2>
    </div>
    <table>
      {#each events as week}
        <tr>
          {#each week as day}
            <Date data={day}/>
          {/each}
        </tr>
      {/each}
    </table>
    <p class="footer">Vairak informācijas Ruckas mižas sociālajos tīklos vai rakstot
      uz e-pastu <strong>ruckasm@gmail.com</strong> vai zvanot uz tel. <strong>29437258</strong> (Sanita), <strong>26496004</strong> (Margarita)
    </p>
  </div>
</main>
<footer>

</footer>

<style>

  main {
    background-color: var(--black-transparent);
    height: 100vh;
    width: min(1200px, 88vw);
    margin: 0 auto;
    position: relative;
    color: var(--white-darker);
  }

  .inner-content {
    padding: 40px 40px 0 100px;
    height: 100vh;
    overflow-y: scroll;
  }

  #logo {
    display: block;
    position: absolute;
    width: 150px;
    top: 0px;
    left: 0px;
    transform: translateX(-50%);
    z-index: 500;
  }

 

  .header-distributer {
    display: flex;
    justify-content: space-between;
    align-items: end;
    padding-bottom: 7px;
  }

  h1 {
    font-family: var(--accent-font);
    font-size: 2rem;
  }

  h2 {
    font-size: 1.2rem;
    font-weight: 400;
  }

  table {
    border-collapse: collapse;
    border: 1px solid var(--white-transparent);
    width: 100%;
  }

  .footer {
    padding-top: 15px;
  }

  @media (max-width: 1200px) {
    #logo{
      transform: translateX(0);
    }

    main {
      width: 92vw;
    }

    .inner-content {
      padding: 40px 40px 0 40px;
    }

    .header-distributer {
    display: flex;
    flex-direction: column;
    gap:7px;
    padding-bottom: 7px;
    }
  }

  @media (max-width: 820px) {
    main {
      width: 100vw;
    }

    .inner-content {
      padding: 40px 20px 0 20px;
    }

    .header-distributer {
      display: flex;
      flex-direction: column;
      gap:7px;
      padding-bottom: 7px;
    }
  }

  @media (max-width: 820px) {
    .inner-content {
      padding: 40px 20px 0 20px;
    }

    h1 {
      font-size: calc(1.3rem + 1vw);
    }

    h2 {
      font-size: calc(0.7rem + 1vw);
    }

    .footer {
      font-size: calc(0.5rem + 1vw);
    }
  }

  @media (max-width: 580px) {
    #logo {
      width: calc(80px + 10vw);
    }

    .inner-content {
      padding: 20px 15px 0 15px;
    }

    .header-distributer {
      margin-bottom: 10px;
    }
  }

  @media (max-width: 470px) {
    main {
      width: 100vw;
    }

    #logo {
      width: 120px;
    }
    h1 {
      font-size: 1.5rem;
    }

    h2 {
      font-size: 0.9rem;
    }

    .footer {
      font-size: 0.8rem;
    }

    .header-distributer {
      margin-left: 120px;
      text-align: right;
    }
  }

  @media (max-width: 340px) {
    .inner-content {
      padding: 90px 7px 0 7px;
    }
    .header-distributer {
      margin-left: 0px;
      text-align: left;
    }
  }
</style>