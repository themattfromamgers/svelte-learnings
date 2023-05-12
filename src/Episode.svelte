<script>
    let name;
    let xd = false;
    let cities = ['İstanbul', 'Angara', 'İzmir']
    let selected = 'İstanbul'
    let selectedSize = '';
    let sizes = ['M', 'L', 'XS', 'SM']
    let firstName = ''

    const submitHandle = ()=>{
        console.log(`isim: ${firstName}`)
    }
</script>

<div>
    <h1>{name}</h1>
    <h2>EPİSODE 2</h2>
    <input type="text" bind:value={name}>

    
    <input type="checkbox" bind:checked={xd}>
    <br>
    <button disabled={!xd}>JAB</button>
    <h3>{JSON.stringify(xd)}</h3>
    <br><br><br>

    <select bind:value={selected}>
        {#each cities as city (city)}
        <option value={city}>{city}</option>
        {/each}
    </select>
    {JSON.stringify(selected)}

    <br>
    <br>
    

    <label>
        {#each sizes as size }
            
            <input type="radio" bind:group={selectedSize} value={size}>
            {size}
        {/each}

    </label>
    {JSON.stringify(selectedSize)}

    <br>
    <br>

    <form action="" on:submit|preventDefault={submitHandle}>
        {firstName}
        <input type="text" bind:value={firstName}>
        <button>Gönder</button>
    </form>
</div>