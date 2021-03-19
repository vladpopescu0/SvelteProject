<script>
	let m = { x:4, y:3};


	function handleMousemove(event) {
		m.x = event.clientX;
		m.y = event.clientY;
	}		
</script>


<style>
	div { width: 100%; height: 100%; }
</style>
<h1 >Sunt tigan</h1>
<div on:mousemove="{e => m = {x: e.clientX,y:e.clientY}}">
	The mouse position is {m.x} x {m.y}
</div>

