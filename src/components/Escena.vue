<template>
	<div class="text-box">
		<div v-for="(data,id) in myTextData" :key="id" :class="{current: id=== activeItem}">
			<div class="text-border">{{data.text}}</div>
			<button  @click="currentSentence(id)">make item active</button>
		</div>
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
			currentSentence(i){
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
