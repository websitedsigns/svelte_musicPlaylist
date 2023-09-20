<script lang="ts">

  import SvgIcon from '@jamescoyle/svelte-icon';

  import { mdiMusic, mdiPlay, mdiPause } from '@mdi/js';



  export let track: Track;

</script>



<li class="flex flex-row px-3 py-2 space-x-4 mb-2">

  <div class="w-12 h-12 text-neutral-400 p-2 border border-neutral-400" aria-hidden="true">

    <SvgIcon type="mdi" path={mdiMusic} />

  </div>

  <div class="flex-1">

    <div class="flex flex-row">

      <h2 class="flex-1 font-bold">{track.title}</h2>

      <p class="text-neutral-200">{track.length}</p>

    </div>

    <p>{track.artist} - {track.album}</p>

  </div>

  <button class="w-12 h-12 p-2" aria-label="Pause playing this track">

    <SvgIcon type="mdi" path={mdiPause} />

  </button>

</li>