<script>
	let m = { x:3, y:3};


	function handleMousemove(event) {
		m.x = event.clientX;
		m.y = event.clientY;
	}		
</script>


<style>
	div { width: 100%; height: 100%; }
</style>

<div on:mousemove="{e => m = {x: e.clientX}}">
	The mouse position is {m.x} x {m.y}
</div>