<template>
	<div class="bottons-box">
		<button @click="$emit('decrementarSentence')">Anterior</button>
		<button @click="$emit('incrementarSentence')">Següent</button> -->
		<!-- <button @click="currentBotton($event)">Anterior</button>
		<button @click="currentBotton($event)">Següent</button> -->
	</div>
</template>

<script>
	export default {
		methods:{
			// currentBotton(e){
			// 	console.log(e.target.innerHTML)
			// },
			incrementarSentence(i){
				this.activeItem = i++;
			},
			decrementarSentence(i){
				this.activeItem = i--;
			}
		}
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
