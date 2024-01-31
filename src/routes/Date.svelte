<script>
  import Event from "./Event.svelte";
  
  export let data;
  
</script>

<td>
  {#if data.showMonth}
    <p class="date-info">{data.month}</p>
  {/if}
  <h class="date-number">{data.date}</h>
  <div class="content">
    {#each data.events as event}
      <Event event={event} date={{month: data.month, day: data.date, count: data.eventCount}}/>
    {/each}
    
  </div>
  
</td>

<style>
  td {
    border: 1px solid var(--white-transparent);
    width: 14.29%;
    height: max(16vh, 130px);
    position: relative;
  }

  .date-number {
    font-size: 1.3rem;
    font-family: var(--accent-font);
    position: absolute;
    top:0;
    right: 10px;
  }

  @media (max-width: 850px) {
    .date-number {
      right: 6px;
    }
  }

  .date-info {
    font-size: 0.9rem;
    font-family: var(--accent-font);
    position: absolute;
    top:5px;
    left: 10px;
  }

  .content {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
  }

  @media (max-width: 980px) {
    .date-info {
      display: none;
    }
  }

  @media (max-width: 600px) {
    td {
      height: 110px;
    }
  }

  @media (max-width: 490px) {
    td {
      height: 100px;
    }
  }

  @media (max-width: 400px) {
    td {
      height: 90px;
    }
  }
  
</style>