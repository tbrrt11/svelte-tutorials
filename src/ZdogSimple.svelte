<script>
	import { onMount } from 'svelte';
	import Zdog from "zdog";

	let illo;

	onMount(async () => {
		illo = new Zdog.Illustration({
			element: '.zdog-canvas',
			rotate: {
				y: 0.03,
				x: 0
			}
		});

		new Zdog.Ellipse({
			addTo: illo,
			diameter: 80,
			stroke: 20,
			color: '#636'
		});
		illo.updateRenderGraph();
		animate()
	});

	const animate = () => {
		illo.rotate.y += 0.03;
		illo.rotate.x += 0.03;
		illo.updateRenderGraph();
		requestAnimationFrame(animate);
	};

</script>

<main>
	<svg class="zdog-canvas" height="250" width="250"></svg>
	<button on:click={animate}>Activate</button>
</main>

<style>
	.zdog-canvas {
		background-color: #ffddfd;
	}
</style>