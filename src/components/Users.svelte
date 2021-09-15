<script>
import { onMount } from "svelte";


export let users = [{name: "janne"}, {name: "jenni"}]

onMount(() => {
    const fetchUsers = async () => {
        let returnData = await fetch('http://localhost:3000/users').then(res => res.json()).then(data => data)
        return returnData
    }

    users = fetchUsers()
    console.log(users)
})
</script>

<style>

</style>

<div>
    {#each users as user}

    <div>
        {user.name}
    </div>

    {:else}
     <div>
         Hämtar användare...
     </div>
    {/each}

</div>