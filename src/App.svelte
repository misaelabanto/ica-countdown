<script lang="ts">
	import { DateTime } from 'luxon';
	import Timer from './components/timer.svelte';
	let days: number;
	let hours: number;
	let minutes: number;
	let seconds: number;
	const leaveDate = DateTime.fromISO('2023-01-20T19:00:00Z')
	function updateTimer() {
		const timeDiff = leaveDate.diffNow('minutes').shiftTo('days', 'hours', 'minutes', 'seconds')
		days = timeDiff.days
		hours = timeDiff.hours
		minutes = timeDiff.minutes
		seconds = timeDiff.seconds
	}
	updateTimer()
	setInterval(() => {
		updateTimer()
	}, 1000)
</script>

<main class='bg-gray-800 h-screen flex justify-center'>
	<div class='flex items-center'>
                <Timer days={days} hours={hours} minutes={minutes} seconds={seconds} />
	</div>
</main>

<style windi:preflights:global windi:safelist:global>
</style>
