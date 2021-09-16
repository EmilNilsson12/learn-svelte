<script>
    // Alert
    function handleClick({ target }) {
        alert('clicked: ' + target.id);
    }
</script>

<div>
    <h3>With stopPropagation</h3>
    <button id="outer btn" on:click={handleClick}>
        Outer button<button
            id="inner btn"
            on:click|stopPropagation={handleClick}
            >Inner button, click to test stopPropagation</button
        >
    </button>
</div>

<div>
    <h3>Without stopPropagation</h3>
    <button id="outer btn" on:click={handleClick}>
        Outer button<button id="inner btn" on:click={handleClick}
            >Inner button, click to test stopPropagation</button
        >
    </button>
</div>
