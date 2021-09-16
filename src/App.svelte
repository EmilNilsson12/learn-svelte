<script>
    let index = 0;
    async function getWorkoutData() {
        const res = await fetch(
            `https://612896ae86a213001729f9c0.mockapi.io/objWithoutArrayValues`
        );
        const text = await res;

        if (res.ok) {
            return text.json();
        } else {
            throw new Error(text);
        }
    }

    let promise = getWorkoutData();

    function handleClick() {
        promise = getWorkoutData();
    }
</script>

<button on:click={handleClick}> Get workout data </button>

<!-- replace this element -->
{#await promise}
    <p>Waiting...</p>
{:then number}
    <pre>The number is {JSON.stringify(number[0], null, 2)}</pre>
{:catch error}
    <p>Error was caught</p>
{/await}
