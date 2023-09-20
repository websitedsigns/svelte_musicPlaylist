<script lang="ts">
  import PlaylistItem from './lib/PlaylistItem.svelte';
  const tracks = [

    {
      id: 1,
      title: 'Track title',
      artist: 'Artist Name',
      album: 'Album Name',
      length: '4:23',
    },

    {
      id: 2,
      title: 'Track title',
      artist: 'Artist Name',
      album: 'Album Name',
      length: '4:23',
    },

    {
      id: 3,
      title: 'Track title',
      artist: 'Artist Name',
      album: 'Album Name',
      length: '4:23',
    },

  ] as Track[];
  let currentTrack = -1;
</script>



<div class="min-h-screen bg-slate-800 text-white">
  <main class="max-w-screen-md mx-auto">
    <header class="bg-pink-600 text-2xl font-bold p-3">
      <h1>Sounds Good! - Epic Playlist</h1>
    </header>
    <ol class="border-4 border-pink-600">
      {#each tracks as track}
        <PlaylistItem
          track={track}
          state={track.id === currentTrack ? 'playing' : 'paused'}
          on:click={() => { track.id === currentTrack ? currentTrack = -1 : currentTrack = track.id; }}/>
      {/each}
    </ol>
  </main>
</div>