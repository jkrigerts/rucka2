<script>
  import Coin from "./Coin.svelte";
import Mail from "./Mail.svelte";
import Phone from "./Phone.svelte";

  export let type;
  export let color;
</script>

{#if type == "phone"}
  <a href="tel:+37128237566" class={color}><Phone />Zvanīt</a>
{:else if type == "email"}
  <a href="mailto:ruckasm@gmail.com" class={color}><Mail />Rakstīt</a>
{:else}
  <a href="{type}" class={color}><Coin />Pirkt</a>
{/if}


<style>
  a {
    display: flex;
    align-items: center;
    gap:5px;
    color: white;
    text-decoration: none;
    cursor: pointer;
    font-family: inherit;
    background-color: inherit;
    padding: 5px 7px;
    border-radius: 1px;
    font-size: 0.9em;
    transition: all 0.3s;
  }

  a:hover {
    transform: translateY(2px);
    filter: brightness(0.95);
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
</style>