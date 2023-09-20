<script lang="ts">

  import PlaylistItem from './lib/PlaylistItem.svelte';

</script>



<div class="min-h-screen bg-slate-800 text-white">

  <main class="max-w-screen-md mx-auto">

    <header class="bg-pink-600 text-2xl font-bold p-3">

      <h1>Sounds Good! - Epic Playlist</h1>

    </header>

    <ol class="border-4 border-pink-600">

      <PlaylistItem/>

      <PlaylistItem/>

      <PlaylistItem/>

    </ol>

  </main>

</div>