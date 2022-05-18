<template>
	<div>
		<button @click='getposts'>Load post</button>
		<div class="postWrapper">
			<div id="card" v-for="post in posts" :key='post.id'>
				<h2>{{post.title}}</h2>
				<p>{{post.body}}</p>
			</div>
		</div>
	</div>


</template>


<script>

import axios from 'axios';

export default {
	name: 'postlist',
	data() {
		return {
			posts: []
		}
	},
	methods: {
		getposts() {
			axios.get('https://jsonplaceholder.typicode.com/posts')
			.then( (res) => {
				console.log(res.data);
				this.posts = res.data;
			})
			.catch( (e) => {
				console.log(e)
			})
		}
	}
}
</script>



<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

	.postWrapper {
		display: flex;
		justify-content: space-around;
		flex-wrap: wrap;
	}

	#card{
		max-width: 300px;
		padding:  10px;
		box-shadow: 4px 4px 20px #ddd;
		margin: 20px;
	}
</style>