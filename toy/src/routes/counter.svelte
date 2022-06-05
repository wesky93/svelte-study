<script lang="ts">
	let result: number = 0;
</script>

<div class="container">
	<button id="subtraction" on:click={() => result--}>-</button>
	<div id="result">{result}</div>
	<button id="plus" on:click={() => result++}>+</button>
</div>
<div class="container">
	<button id="plus" on:click={() => (result = 0)}>Reset</button>
</div>

<style lang="postcss">
	.container {
		@apply flex justify-around pt-6;

		button {
			@apply h-10 px-6 rounded-md border text-lg font-semibold border-slate-200 
                bg-white text-slate-900 
                hover:bg-slate-900 hover:text-white
                active:bg-slate-600;
		}
		#result {
			@apply text-lg font-semibold pt-2;
		}
	}
</style>
