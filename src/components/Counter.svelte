<script>
	let count1 = 0;
	let count2 = 0;
    let count3 = 0;
    let product = 0;

	$: {
        if(product > 100) {
            console.log("big number")
            count1 = 0
            count2 = 0
            count3 = 0
        }
        product = count1 * count2 * count3
    }

	function handleClick1() {
		count1 += 1;
	}
	function handleClick2() {
		count2 += 1;
	}
	function handleClick3() {
		count3 += 1;
	}
</script>

<div>
    <button on:click={handleClick1}>
        Clicked {count1} {count1 === 1 ? 'time' : 'times'}
    </button>

    <button on:click={handleClick2}>
        Clicked {count2} {count2 === 1 ? 'time' : 'times'}
    </button>

    <button on:click={handleClick3}>
        Clicked {count3} {count3 === 1 ? 'time' : 'times'}
    </button>

    <p>
        {count1} times {count2} times {count3} is {product}
    </p>
</div>
