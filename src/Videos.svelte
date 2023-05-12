<script>

let duration, ended, currentTime, paused = true, muted=false;
let secondsFormat = (seconds=0)=>{
    return new Date(1000 * seconds)
    .toISOString()
    .substr(14.5)
}

</script>

<div>
    <h1>MP4</h1>
    <video
    bind:duration={duration} 
    bind:currentTime={currentTime} 
    bind:ended={ended}
    bind:paused={paused}
    bind:muted={muted}
    src="https://sveltejs.github.io/assets/caminandes-llamigos.mp4" controls>
    </video>


<input type="range" min="0" max={duration} bind:value={currentTime}>
{ended ? "evet": "hayır"}
{secondsFormat(duration)}
<button on:click={()=> paused = !paused}>{paused ? "oynat": "durdur"}</button>
<button on:click={()=> muted = !muted}>{muted ? "sesi aç": "sesi kapat"}</button>
</div>