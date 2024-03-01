<script>
  import events from "$lib/data/events.json";
  import Date from "./Date.svelte";
  import Facebook from "./Facebook.svelte";
  import Instagram from "./Instagram.svelte";

</script>

<main>
  <img src="logo.png" alt="Ruckas muiža" id="logo"/>
  <div class="inner-content">
    <div class="header-distributer">
      <h1>Ruckas muiža ielūdz!</h1>
      <h2>2024. gada MARTA <strong>PASĀKUMU KALENDĀRS</strong></h2>
    </div>
    <p class="explanation">Uzziniet vairāk, izvēloties krāsaino datumu</p>
    <table>
      {#each events as week}
        <tr>
          {#each week as day}
            <Date data={day}/>
          {/each}
        </tr>
      {/each}
    </table>
    <p class="footer">Vairāk informācijas Ruckas muižas sociālajos tīklos vai rakstot
      uz e-pastu <strong><a href="mailto:kultura@ruckasmuiza.lv">kultura@ruckasmuiza.lv</a></strong> vai zvanot uz tel. <strong><a href="tel:+37129437258">+371 28237566</a></strong>
    </p>
    <p>Mājaslapa vēl ir izstrādes stadijā.</p>
    <div class="social-sm">
      <a href="https://www.facebook.com/profile.php?id=61551705841167" target="_blank"><Facebook /></a>
      <a href="https://instagram.com/ruckas.muiza?igshid=OGQ5ZDc2ODk2ZA==" target="_blank"><Instagram /></a>
    </div>
  </div>
  <div class="social">
    <a href="https://www.facebook.com/profile.php?id=61551705841167" target="_blank"><Facebook /></a>
    <a href="https://instagram.com/ruckas.muiza?igshid=OGQ5ZDc2ODk2ZA==" target="_blank"><Instagram /></a>
  </div>
</main>

<style>

  main {
    background-color: var(--black-transparent);
    min-height: 100vh;
    width: min(1200px, 88vw);
    margin: 0 auto;
    position: relative;
    color: var(--white-darker);
  }

  .inner-content {
    padding: 40px 40px 10px 100px;
    min-height: 100vh;
    /* overflow-y: scroll; */
    position: relative;
  }

  #logo {
    display: block;
    position: absolute;
    width: 150px;
    top: -1px;
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

  .social, .social-sm {
    display: flex;
  }

  .social {
    position: absolute;
    bottom: 15px;
    left: -3.5vw;
    flex-direction: column;
    gap: 10px;
  }

  .social-sm {
    margin-top: 10px;
    margin-left: -5px;
    gap: 20px;
    flex-direction: row;
    display: none;
  }

  .social > a, .social-sm > a {
    color: inherit;
  }

  table {
    border-collapse: collapse;
    border: 1px solid var(--white-transparent);
    width: 100%;
    table-layout: fixed;
  }

  .footer {
    padding-top: 15px;
  }

  .footer a {
    color: inherit;
  } 

  @media (max-width: 1200px) {
    #logo{
      transform: translateX(0);
    }

    main {
      width: 92vw;
    }

    .inner-content {
      padding: 40px 40px 10px 40px;
    }

    .header-distributer {
    display: flex;
    flex-direction: column;
    gap:7px;
    padding-bottom: 7px;
    }
  }

  @media (max-width: 940px) {
    .social {
      display: none;
    }

    .social-sm {
      display: flex;
    }
  }

  @media (max-width: 820px) {
    main {
      width: 100vw;
    }

    .inner-content {
      padding: 40px 20px 20px 20px;
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
      padding: 40px 20px 20px 20px;
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
      padding: 20px 15px 20px 15px;
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

    .footer, .explanation {
      font-size: 0.95rem;
    }

    .header-distributer {
      margin-left: 120px;
      text-align: right;
    }
  }

  @media (max-width: 340px) {
    .inner-content {
      padding: 90px 7px 20px 7px;
    }
    .header-distributer {
      margin-left: 0px;
      text-align: left;
    }
  }
</style>