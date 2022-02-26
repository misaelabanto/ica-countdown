<script lang="ts">
	import Unit from './unit.svelte';
	export let days: number;
	export let hours: number;
	export let minutes: number;
	export let seconds: number;
</script>

<div>
	<p class='text-green-500 text-5xl text-center'>La diversión comenzará en:</p>
	<div class="flex flex-wrap justify-center gap-2 m-sm-2">
		<Unit value={days} unit="días" />
		<Unit value={hours} unit="horas" />
		<Unit value={minutes} unit="min." />
		<Unit value={seconds} unit="seg." />
	</div>
</div>

<style>
</style>
