<script lang="ts">
	import { Slider } from 'melt/builders';

	const slider = new Slider({ min: 0, max: 4, step: 1, value: 0 });

	const sliderToSigmaMap: { [key: number]: string } = {
		0: '3.5',
		1: '4.0',
		2: '4.5',
		3: '5.0',
		4: '5.5'
	};

	const sigma = $derived(sliderToSigmaMap[slider.value]);
</script>

<h2>Experiments: Hyperparameter Study</h2>

<div class="picker">
	𝜎: {sigma}

	<div {...slider.root} class="slider">
		<div class="track">
			<div class="thumb" {...slider.thumb}></div>
		</div>
	</div>

	<img src="stitched_sigma_{sigma}.png" alt="sigma ablation study" height="800" width="800" />
</div>

<style>
	.picker {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.slider {
		width: 100%;
		max-width: 200px;
		position: relative;
	}

	.track {
		height: 4px;
		background: #e2e8f0;
		position: relative;
	}

	.thumb {
		position: absolute;
		left: var(--percentage);
		top: 50%;
		transform: translate(-50%, -50%);
		width: 16px;
		height: 16px;
		background: #3b82f6;
		border-radius: 50%;
	}

	img {
		height: 800px;
	}
</style>
