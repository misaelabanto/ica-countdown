<script lang="ts">
  export let value: number;
  export let unit: string;
</script>

<div class='w-auto'>
  <div class='flex'>
    <div class='text-8xl text-yellow-300'>{Math.round(value)}</div>
    <div class='text-4xl align-bottom text-yellow-300'>{unit}</div>
  </div>
</div>

<style>
</style>