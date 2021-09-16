<script>
    import { onMount } from "svelte";
    import User from './User.svelte'
    
    
    
    
    onMount(() => {
            fetch('http://localhost:3000/users')
            .then(res => res.json())
            .then(data => {
                console.log('data: ', data)
                users = data
            })
        })


    export let users = [
        {
            first_name: "janne", 
            last_name: "kemi"
        }, 
        {
            first_name: "jenni", 
            last_name: "pulli"
        }
    ]
</script>


    
<style>

    main {
        display: grid;
        grid-template-columns: minmax(100px, 1fr) minmax(auto, 600px) minmax(100px, 1fr);
        background-color: blueviolet;
    }

    .my-grid {
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        grid-gap: 10px;
        margin-top: 30px;
    }  
</style>
    
<main>
    <aside>
        
    </aside>
    <div class='my-grid'>
        {#each users as user}
        <User {user}/>
        
        {:else}
        <div>
            Hämtar användare...
        </div>
        {/each}
        
    </div>
    
    <aside>

    </aside>
</main>