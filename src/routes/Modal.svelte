<script>
  import { fade, scale } from 'svelte/transition';
  import Close from "./Close.svelte";
  export let event;
  export let date;
  export let close;
</script>


<button class="wrapper" on:click={close} transition:fade>
</button>

<div class="modal" transition:scale>
  <button class={`close ${event.color}`} on:click={close}>
    <Close />
  </button>
  <p>{event.type}</p>
  <h2 class={event.color}>{event.titleLong != "" ? event.titleLong : event.title}</h2>
  <p>{date.day}. {date.month.toLowerCase()}</p>
  <p>{event.timeLong ? event.timeLong : event.time}</p>
  <p class="description">{event.infoLong}</p>
  <p class="price">{event.price}</p>
</div>


<style>
  .wrapper {
    position: fixed;
    top:0;
    left:0;
    width: 100vw;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: var(--black-transparent);
    z-index: 1000;
    backdrop-filter: blur(2px);
    border: none;
  }

  .modal {
    background-color: var(--white-darker);
    width: 320px;
    height: 400px;
    z-index: 1001;
    position: fixed;
    top:50%;
    left:50%;
    transform: translateX(-50%) translateY(-50%);
    padding: 20px 15px;
    color: var(--black);
  }

  h2 {
    font-family: var(--accent-font);
    margin-bottom: 10px;
  }

  .green {
    color: var(--dabas-zala);
  }
  .blue {
    color: var(--debess-zila);
  }
  .gray {
    color: var(--akmens-peleka);
  }
  .brown {
    color: var(--mala-bruna);
  }
  .red {
    color: var(--avenu-sarkana);
  }
  .yellow {
    color: var(--smilsu-dzeltena);
  }

  .close {
    position: absolute;
    cursor: pointer;
    border: none;
    top:3px;
    right:3px;
    background: none;
  }

  .description, .price {
    margin-top: 20px;
  }

  @media (max-width: 340px) {
    .modal {
      width: 90vw;
    }
  }

</style>