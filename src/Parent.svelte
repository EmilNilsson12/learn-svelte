<script>
    import Child from './components/Child.svelte';

    const childProps = {
        name: 'Svelte',
        version: 3,
        speed: 'blazing',
        website: 'https://svelte.dev',
    };
</script>

<style></style>

<main>
    <div>Main element</div>
    <Child {...childProps} />
    <Child />
</main>
