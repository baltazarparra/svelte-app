<script>
    let count = 0

    function increment() {
        count += 1
    }

    function decrement() {
        count -= 1
    }
</script>

<div>
    Current count: <input bind:value={count} type="number" />
</div>

{#if count > 5}
    <p>Pouco</p>
{:else if count < -5}
    <p>Muito pouco</p>
{/if}

<button on:click={increment}>Increment</button>
<button on:click={decrement}>Decrement</button>