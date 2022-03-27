<script>
     export let text;
     export let checked;
     export let removeItem;
     export let toggleDone
</script>

<li class="list-item">
     <input bind:checked={checked} on:change={toggleDone} type="checkbox"> 
     <span class="checked-item" class:checked={checked}>{text}</span>
     <button type="button" class="x-button" on:click={removeItem}>X</button>
</li>

<style>
     .checked {
          text-decoration: line-through;
          color: #ec4a93;
     }
     .list-item {
          color: #2e6fd1;
          background-color: #EEBA0B;
          font: 1.4em 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
          font-weight: 800;
          margin: 1rem;
          padding: .5rem;
          border-radius: 5px;                    
     }
     .x-button {
          color: indigo;
          background-color: #C5E6A6;
          width: 3rem;          
          margin: 0 0 0 1.5rem;
          border-radius: 5px;         
     }
     .x-button:hover {
          background-color: #ee372a;
          color: aliceblue;
     }


</style>