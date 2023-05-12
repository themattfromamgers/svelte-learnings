<script>
    let todos = [
        {
            id: 1,
            name: 'Todo 1',
            done: false
        },
        {
            id: 2,
            name: 'Todo 1',
            done: true
        },
        {
            id: 3,
            name: 'Todo 1',
            done: false
        }
    ]
</script>

{#each todos as todo}
    <input type="checkbox" checked={todo.done}>
    <div>{todo.name}</div>
{/each}

<style>
    input {
        border: 1px solid gray;
    }
</style>