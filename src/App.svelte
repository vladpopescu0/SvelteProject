<script>
	import Ceva from './Ceva.svelte'
	let value1 = 0;
	$: ceva = 0;

	function addValue(){
		ceva=Number(ceva)+Number(value1)
	}
	function minusValue(){
		ceva = Number(ceva)-Number(value1)
	}
	function multiplyValue(){
		ceva = Number(ceva)*Number(value1)
	}
	function divideValue(){
		ceva=(Number(ceva)/Number(value1)).toFixed(3)
	}
	function laLoc(){
		value1=0
	}
</script>
	<input class="center-block" bind:value={value1}>
	
	<h1 class="bazat">Rezultatul este: {ceva}</h1>
	
	<style>

		.bazat {
			text-align: center;
			align-self: center;
		}
		.center-block {
			margin: auto;
			display: block;
		}
		button {
			margin:auto;
			display:block;
			height:4rem;
			width: 8rem;
			background-color: yellow;
		}


	</style>
	
<Ceva on:click={addValue} on:click={laLoc}/>
<button on:click={minusValue} on:click={laLoc}>
		-
</button>
<button on:click={multiplyValue} on:click={laLoc}>*</button>
{#if value1!==0}
<button on:click={divideValue} on:click={laLoc}>/</button>
{/if}