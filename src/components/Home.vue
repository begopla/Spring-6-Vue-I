<template>
	<div class="parent-box">
		<Botons />
		<Escena  ></Escena>
	</div>
</template>

<script>
import Escena from './Escena.vue';
import Botons from './Botons.vue';
	export default {
		name:'App',
		components: {
			Escena,
			Botons
		},



	}
</script>

<style lang="css" scoped>
	.parent-box{
		height: 100vh;
		/*background-color: green;
*/
	}
</style>
