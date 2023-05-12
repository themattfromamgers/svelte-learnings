<script>
    let amk;
    $: dobule = count * 2
    $: console.log('count', count)
    $: if(count > 5){
        amk = 'büyük değer'
    }

    $:{
        console.log(count)
    }

    let count = 0;
    const clickHandle=()=>{
        count += 1
    }

</script>

<div>
    <h1>{count}</h1>
    <button on:click={clickHandle}>Buttons</button>
    <h3>{amk}</h3>
    <h3>{dobule}</h3>
</div>

<style>

</style>