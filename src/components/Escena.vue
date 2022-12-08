<template>
	<div class="text-box">
		<!-- <p>El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial.</p> -->
		<div v-for="(data, i) in myTextData" :key="data.id" :class="{current: i=== activeItem}">
			<div class="text-border">{{data.text}}</div>
		</div>
		<button @click="selectItem(i)">make item active</button>
	</div>
</template>

<script>
import textData from '../../data/data.json';

export default {
	data(){
		return{
			myTextData: textData,
			activeItem: null
		};
	},
	methods: {
		selectItem(i){
			console.log(i);
			this.activeItem = i;
		}
	}
}
</script>

<style lang="css" scoped>
	.text-box{
		padding-top: 1vh;
	}
	.text-border{
		border-radius: 1.5rem;
		margin-top: 2vh;
		padding: 1vh;
		margin-left:2vw;
		margin-right: 2vw;
		border: 2px solid black;
	}
	.current{
		background-color: rgba(206, 117, 117, 0.49);
	}

</style>
