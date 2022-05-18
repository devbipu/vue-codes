<template>
	<div id="card">
		<h2>Tab A content</h2>
	</div>
</template>


<script>
export default {
	name: 'Tab-A',
	data() {
		return {
			
		}
	},
	beforeCreate() {
		console.log('Child beforeCreate')
	},
	created() {
		console.log('Child created')
	},
	beforeMount() {
		console.log('Child beforeMount')
	},
	mounted() {
		console.log('Child mounted')
	},
	beforeUpdate() {
		console.log('Child beforeUpdate')
	},
	updated() {
		console.log('Child Update')
	},
	beforeUnmount() {
		console.log('Child beforeUnmount')
	},
	unmounted(){
		console.log('Child unmouned')
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