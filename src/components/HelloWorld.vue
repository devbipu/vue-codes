<template>
	<div id="card">
		<p v-for='name in names'>
			<slot :fname='name.fname' :lname='name.lname'></slot>
		</p>
	</div>
</template>


<script>
export default {
	name: 'HelloWorld',
	data() {
		return {
			names: [
				{
					fname: "Biplob",
					lname: "Shaha",
				},
				{
					fname: "Mr A",
					lname: "Shaha",
				},
				{
					fname: "Mr B",
					lname: "Shaha",
				}
			]
		}
	}
}
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	h1, h2 {
		font-weight: normal;
	}
	ul {
		list-style-type: none;
		padding: 0;
	}
	li {
		display: inline-block;
		margin: 0 10px;
	}
	a {
		color: #42b983;
	}

	#card{
		max-width: 300px;
		padding:  10px;
		box-shadow: 4px 4px 20px #ddd;
		margin: 20px;
	}
</style>