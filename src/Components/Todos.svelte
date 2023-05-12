<script>
  import { each } from "svelte/internal";


    let todos = ['todo', 'todo 2', 'todo 3']
    let xd = [
        {
            id: 1,
            title: "todo 1"
        },
        {
            id: 2,
            title: "todo 2"
        }
    ]
</script>


<div>
    {#each todos as todo, i}
        <li> {todo} {i} </li>
    {/each}



    {#each Array(5) as i}
        <p>hello there</p>
    {/each}
    
    {#each xd as {id, title}, i}

        <li>{title} {id}</li>
    {/each}

</div>


