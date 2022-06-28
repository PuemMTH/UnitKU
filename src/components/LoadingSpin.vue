<template>
<div class="relative ...">
  <p>Relative parent</p>
</div>
</template>

<script>
	export default {
		name: 'LoadingSpin',
	}
</script>

<style>
	div.masked {
		position: relative;
	}

	div.masked:before {
		position: absolute;
		content: '';
		width: 100%;
		height: 100%;
		background-color: rgb(114, 110, 110, 0.7);
	}

	span.ping {
		background-color: rgb(143, 174, 144);
	}
</style>
