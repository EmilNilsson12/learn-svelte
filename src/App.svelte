<script>
    import Users from './components/Users.svelte';
    import Counter from './components/Counter.svelte';
</script>

<style>
    main {
        text-align: center;
        /* padding: 1em; */
        /* max-width: 240px; */
        margin: 0;
        padding: 0;
    }

    h1 {
        color: #ff3e00;
        text-transform: uppercase;
        font-size: 4em;
        font-weight: 100;
    }

    @media (min-width: 640px) {
        main {
            max-width: none;
        }
    }
</style>

<main>
    <h1>Meet our team!</h1>
    <Counter />
    <Users />
</main>
