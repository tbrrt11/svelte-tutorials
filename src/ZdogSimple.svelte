<script>
	import { onMount } from 'svelte';
	import Zdog from "zdog";

	let illo;

	onMount(async () => {
		illo = new Zdog.Illustration({
			element: '.zdog-canvas',
			zoom: 1,
			dragRotate: true
		});

		new Zdog.Shape({
			addTo: illo,
			path: [ { y: -3 }, { y: 3 } ],
			stroke: 8,
		});

		// patty
		new Zdog.Ellipse({
			addTo: illo,
			diameter: 72,
			stroke: 28,
			color: '#322'
		});

		illo.updateRenderGraph();
		animate();
	});

	const animate = () => {
		illo.updateRenderGraph();
		requestAnimationFrame(animate);
	}

</script>

<main>
	<svg class="zdog-canvas" height="250" width="250"></svg>
</main>

<style>
	.zdog-canvas {
		background-color: #ffddfd;
	}

	.zdog-canvas:hover {
		cursor: pointer;
	}
</style>