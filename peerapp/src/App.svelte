<script>
  import svelteLogo from './assets/svelte.svg'
  import Counter from './lib/Counter.svelte'
  import { Peer } from './lib/peerjs';

  console.log("initializing connnection to peers.");
  var peer =  new Peer();

  

</script>

<main>
  <div>
    <a href="https://vitejs.dev" target="_blank"> 
      <img src="/vite.svg" class="logo" alt="Vite Logo" />
    </a>
    <a href="https://svelte.dev" target="_blank"> 
      <img src={svelteLogo} class="logo svelte" alt="Svelte Logo" />
    </a>
  </div>
  <h1>Peer to peer collaboration</h1>

  <div class="card">
    <Counter />
  </div>

  <p>
  </p>

  <p class="read-the-docs">
    Somehting will go here later.
  </p>
</main>

<style>
  
</style>
