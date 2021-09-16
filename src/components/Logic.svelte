<script>
    let user = { loggedIn: false };

    export let name = '';

    function toggle() {
        user.loggedIn = !user.loggedIn;
    }
</script>

{#if user.loggedIn && name !== ''}
    <p>Welcome {name}!</p>
    <button on:click={toggle}> Log out </button>
{:else if user.loggedIn}
    <p>Welcome Guest!</p>
    <button on:click={toggle}> Log out </button>
{:else}
    <button on:click={toggle}> Log in </button>
{/if}
