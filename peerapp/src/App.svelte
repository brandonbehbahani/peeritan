<script>
  import svelteLogo from './assets/svelte.svg'
  import Counter from './lib/Counter.svelte'
  import { Peer } from './lib/peerjs';

  console.log("initializing connnection to peers.");

  var lastPeerId;
  var peer =  new Peer();

  peer = new Peer(null, { debug: 2 });

  peer.on('open', function (id) {
                        // Workaround for peer.reconnect deleting previous id
                        if (peer.id === null) {
                            console.log('Received null id from peer open');
                        } else {
                            lastPeerId = peer.id;
                        }

                        console.log('ID: ' + peer.id);
                    });



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
