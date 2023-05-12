<script>
    let fontSize = 16, w,h;
    let renk = 'red'
</script>


<div>
    <input type="range" bind:value={fontSize}>
    <input type="text" bind:value={renk}>
    <h3 bind:clientWidth={w} bind:clientHeight={h} style='display: inline-block; font-size: {fontSize}px; background: {renk};'>HELLO THERE</h3>
    size : {w}px and {h}px
</div>