<script>
  import Modal from "./Modal.svelte";
  export let event;
  export let date;

  let open;

  function handleClose() {
    open = false;
  }
</script>

{#if open}
  <Modal event={event} date={date} close={handleClose}/>
{/if}

<button class={`${event.color} e-${date.count}`} on:click={() => open = true}>
  <div>
    <p class={`type e-${date.count}`}>{event.type}</p>
    <p class={`time e-${date.count}`}>{event.time}</p>
    <h4 class={`title e-${date.count}`}>{event.title}</h4>
    {#if event.info != ""}
      <p class={`info e-${date.count}`}>{event.info}</p>
    {/if}
  </div>
</button>

<style>
  button {
    flex-grow: 1;
    display: flex;
    align-items: center;
    text-align: left;
    color: inherit;
    border: none;
    cursor: pointer;
    padding: 0 15px;
  }
  button:hover {

  }

  .e-3:first-child, .e-2:first-child {
    padding-right: 25px;
  }

  p {
    font-size: 0.5rem;
  }

  h4 {
    font-size: 0.7rem;
    font-family: var(--accent-font);
    line-height: 1.2;
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

  @media (max-width: 1270px) {
    button {
      padding: 0 7px;
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
    button {
      padding: 0 10px;
    }
  }

  @media (max-width: 850px) {
    .title.e-3, .title.e-2{
      font-size: calc(0.4rem + 0.5vw);
    }
  }

  @media (max-width: 700px) {
    .title.e-3, .title.e-2{
      font-size: 0.6rem;
    }
  }

  @media (max-width: 600px) {
    .time.e-1, .title.e-3, .title.e-2{
      display: none;
    }
    .title.e-1{
      font-size: calc(0.4rem + 0.5vw);
    }
    button {
      padding: 0 5px;
    }
  }

  @media (max-width: 540px) {
    .title.e-1{
      display: none;
    }
  }

</style>