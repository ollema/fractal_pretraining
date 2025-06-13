<script lang="ts">
	import { Slider } from 'melt/builders';

	const slider = new Slider({ min: 0, max: 7, step: 1, value: 4 });

	const sliderToDeltaMap: { [key: number]: string } = {
		0: '0.001',
		1: '0.005',
		2: '0.01',
		3: '0.05',
		4: '0.1',
		5: '0.2',
		6: '0.3',
		7: '0.5'
	};

	const delta = $derived(sliderToDeltaMap[slider.value]);
</script>

<h2>Experiments: Hyperparameter Study</h2>

<div class="picker">
	Δ: {delta}

	<div {...slider.root} class="slider">
		<div class="track">
			<div class="thumb" {...slider.thumb}></div>
		</div>
	</div>

	<img src="stitched_{delta}.png" alt="delta ablation study" height="800" width="800" />
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
