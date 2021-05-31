<script>
    let newItem = "";
    
    let todoList = [{text: "Städa rummet", status: true},
                    {text: "Plugga kemi", status: false},
                    {text: "Läsa svenska boken", status: false}];
    
    function addToList() {
        todoList = [...todoList, {text: newItem, status: false}];
        newItem = "";
    }

    function removeFromList(index) {
        todoList.splice(index, 1)
        todoList = todoList;
    }

</script>

<main>
    <input bind:value={newItem} type="text" placeholder="new todo item..">
<button on:click={addToList}>Add</button>
 
</main>
