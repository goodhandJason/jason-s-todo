<script>
     import Item from './Item.svelte';
     let newItem;
     let todoList = [];
     let count = [];
     
     function addToList() {
          if (!newItem) return;
          todoList = [...todoList, {
               text: newItem,
               checked: false,
          }];
          newItem = '';
     }
     function removeFromList(n) {
          todoList.splice(n, 1);
          todoList = todoList;
     }
     function toggleDone(index, v) {
          v = !v;
          todoList[index].checked = v;
          todoList = todoList;
     }

</script>

<h1>Enter an Item To Do!</h1>
<form on:submit|preventDefault={addToList}>
     <input class="textbox" placeholder="Enter an Item!" bind:value={newItem}>
</form>

<ul>
     {#each todoList as item, index}
          <Item 
               text={item.text}
               checked={item.checked}
               toggleDone={() => toggleDone(index, item.checked)}             
               removeItem={() => removeFromList(index)}
          />
     {/each}
</ul>

<style>
     ul{
          list-style: none;
          padding: .5rem;
          margin: .5rem 0 0 0;
          background-color: #F2CEE6;
          border-radius: 15px;                    
     }

     h1 {
          color: #aa00f8;
          font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
          -webkit-text-stroke: 1px #7400aa;                   
     }

     .textbox {
          background-color: #A6D4DE;
          border: #56c4dd solid 5px;
          border-radius: 5px;
     }
</style>