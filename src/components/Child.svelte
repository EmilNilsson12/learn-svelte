<script>
    export let name = 'React';
    export let speed = 'Lazy';
</script>

<style>
    .child {
        border: 1px solid black;
        padding: 4px;
        margin: 14px;
    }
    u {
        background-color: red;
        color: yellow;
        padding: 0 5px;
    }
    .bold {
        font-weight: 900;
    }
</style>

<div class="child">
    <div>Framework: <u>{name}</u></div>
    <div>Speed: <u>{speed}</u></div>
    <div>
        Version: <u>{$$props.version}</u> parsed with
        <span class="bold">$$props.prop</span>
    </div>
</div>
