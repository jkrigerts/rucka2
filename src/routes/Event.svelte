<script>
  import Modal from "./Modal.svelte";
  export let event;
  export let date;

  let open;

  function handleClose() {
    open = false;
  }
</script>

<button class={`${event.color} e-${date.count}`} on:click={() => open = true}>
  <div>
    <p class={`type e-${date.count}`}>{event.type}</p>
    <p class={`time e-${date.count}`}>{event.time}</p>
    <h4 class={`title e-${date.count}`}>{event.title}</h4>
    {#if event.info != ""}
      <p class={`info e-${date.count}`}>{event.info}</p>
    {/if}
  </div>
  {#if event.cancelled}
    <div class="cancelled"></div>
  {/if}
</button>

{#if open}
  <Modal event={event} date={date} close={handleClose}/>
{/if}

<style>
  button {
    flex: 1;
    display: flex;
    align-items: center;
    text-align: left;
    color: inherit;
    border: none;
    cursor: pointer;
    padding: 0 10px;
    position: relative;
    transition: all 0.3s;
  }

  button:active, button:hover {
    /* transform: scale(1.03);
    z-index: 2; */
  }

  button > div {
    overflow: hidden;
  }

  .e-3:first-child, .e-2:first-child {
    padding-right: 20px;
  }

  p {
    font-size: 0.5rem;
  }

  h4 {
    font-size: 0.7rem;
    font-family: var(--accent-font);
    line-height: 1.2;
    padding: 5px 0; 
    text-transform: uppercase;
  }

  .e-3, .e-2 h4 {
    padding: 0; 
  }

  .green {
    background-color: var(--dabas-zala);
  }
  .blue {
    background-color: var(--debess-zila);
  }
  .gray {
    background-color: var(--akmens-peleka);
  }
  .brown {
    background-color: var(--mala-bruna);
  }
  .red {
    background-color: var(--avenu-sarkana);
  }
  .yellow {
    background-color: var(--smilsu-dzeltena);
  }

  .green:hover {
    background-color: var(--dabas-zala-darker);
  }
  .blue:hover {
    background-color: var(--debess-zila-darker);
  }
  .gray:hover {
    background-color: var(--akmens-peleka-darker);
  }
  .brown:hover {
    background-color: var(--mala-bruna-darker);
  }
  .red:hover {
    background-color: var(--avenu-sarkana-darker);
  }
  .yellow:hover {
    background-color: var(--smilsu-dzeltena-darker);
  }

  @media (max-width: 1270px) {
    button {
      padding: 0 10px;
    }
  }

  @media (max-width: 1250px) {
    .info {
      display: none;
    }
    .type {
      display: none;
    }
  }

  @media (max-width: 1150px) {
    .time.e-3, .time.e-2{
      display: none;
    }
    .e-2:first-child {
      padding-top: 20px;
    }
    button {
      padding: 0 10px;
    }
  }

  @media (max-width: 850px) {
    .title{
      font-size: calc(0.4rem + 0.5vw);
    }
    button {
      padding: 0 5px;
    }
  }

  /* @media (max-width: 700px) {
    .title{
      font-size: 0.6rem;
    }
  } */

  @media (max-width: 650px) {
    .time.e-1 {
      display: none;
    }
    .title{
      font-size: calc(0.2rem + 0.9vw);
    }
    button {
      padding: 0 3px;
    }
  }

  @media (max-width: 540px) {
    .e-1:first-child {
      padding-top: 10px;
    }
  }

  .cancelled {
    position: absolute;
    top: 45%;
    left: 50%;
    width: 100%;
    height: 0.9vh;
    background-color: rgb(177, 32, 32);
    background: linear-gradient(90deg, rgba(0,0,0,0) 0%, var(--cancelled) 15% 85%, rgba(0,0,0,0) 100%);
    transform: translateX(-50%) rotate(20deg);
  }

</style>