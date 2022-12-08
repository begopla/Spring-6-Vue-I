<template>
	<div class="bottons-box">
		<button @click="currentSentence(i)">Anterior</button>
		<button @click="currentSentence(i)">Següent</button>
	</div>
</template>

<script>
	export default {

	}
</script>

<style lang="css" scoped>

	.bottons-box{

		padding-top: 2vh;
	}

	button{
		width: 48vw;
		height: 8vh;
	}

</style>
