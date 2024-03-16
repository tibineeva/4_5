<script>
    let newItem = "";
    let todoList = [];
    function add() {
        if (newItem !== "") {
            todoList = [
                ...todoList,
                {
                    задача: newItem,
                    завершено: false,
                },
            ];
            newItem = "";
        }
    }
</script>

<main>
    <h1>My to-do list</h1>
    <form on:submit|preventDefault={add}>
        <input bind:value={newItem} placeholder="Enter to-do" />
        <button class="add-todo" on:click={add}><span>+</span></button>
    </form>
    <div class="todos">
        {#each todoList as item, index}
        <span class="todo__text">{item.task}</span>
        <div class="todo__buttons"></div>
        {/each};
        </div>
    <style>
        .todo {
            display: flex;
            padding: 20px;
            border-radius: 20px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.2);
            background-color: hsla(0, 0%, 100%, 0.2);
            margin-top: 1rem;
            font-size: 1.2rem;
            justify-content: space-between;
            align-items: center;
        }
    
        .todo__buttons {
            display: flex;
            align-items: center;
            margin-left: 1rem;
        }
    
        .todo button {
            width: 32px;
            height: 32px;
            padding: 4px;
            margin: 0;
            flex-shrink: 0;
        }
    
        h1 {
            text-align: center;
            font-size: 1.5rem;
            margin: 2em 0;
        }
    </style>
</main>

<style>
    main {
        display: flex;
        flex-direction: column;
        align-items: center;
        min-height: 100vh;
        padding: 5vmin;
        box-sizing: border-box;
        background: rgb(214, 186, 255);
    }

    form {
        width: 100%;
        max-width: 500px;
        display: flex;
        align-items: center;
        margin-bottom: 1rem;
    }

    input {
        flex-grow: 1;
        width: 0;
        border: none;
        border-bottom: 1px solid black;
        background: transparent;
        box-shadow: none;
        font-size: 1.2rem;
        margin: 0;
        outline: none;
    }
</style>
