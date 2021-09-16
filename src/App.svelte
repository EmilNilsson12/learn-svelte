<script>
    let m = { x: 0, y: 0 };

    function handleMousemove(event) {
        console.log(event.clientX);
        console.log(event.clientY);
        m.x = event.clientX;
        m.y = event.clientY;
    }
</script>

<style>
    div {
        width: 100%;
        height: 100vh;
    }
</style>

<div on:mousemove={handleMousemove}>
    The mouse position is {m.x} x {m.y}
</div>
