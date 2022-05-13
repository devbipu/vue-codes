<template>
	<div>
		<input type="text" v-model="uname">
		<button @click='$emit("close", uname)'>Close</button>
	</div>
</template>


<script>
export default {
	name: 'HelloWorld',
	props: {
		title: {
			type: String,
			required: true,
			default: "This is default title"
		},
		postLike: Number,
		isPublish: Boolean,
	},
	inheritAttrs: false,
	emits: {
		close: (uname) => {
			if (uname == '') {
				return false;
			}else{
				return true;
			}
		}
	},
	data() {
		return {
			uname: '',
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
</style>