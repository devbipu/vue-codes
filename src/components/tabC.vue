<template>
	<div id="card">
		<h2>Tab C content</h2>
		<input type="text" v-model="name">
	</div>
</template>


<script>
export default {
	name: 'Tab-C',
	data() {
		return {
			name: "",
		}
	}
}
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

	#card{
		max-width: 300px;
		padding:  10px;
		box-shadow: 4px 4px 20px #ddd;
		margin: 20px;
	}
</style>