<script>
    // setup code goes here
    import { createEventDispatcher } from 'svelte';

    const dispatch = createEventDispatcher();

    function sayHello() {
        dispatch('message', {
            text: 'Hello!',
        });
    }
</script>

<button on:click={sayHello}> Click to say hello </button>
