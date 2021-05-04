<template>
	<div class="contact">
		<h1>Jobs Page</h1>
		<div v-for="job in jobs" :key='job.id'>
			<router-link :to="{ name: 'Job Detail', params: {id: job.id}}">
				<h2 class="jobs">{{ job.title }}</h2>
			</router-link>
		</div>
		
	</div>
</template>

<script>

export default {
	name: 'Jobs',
	data() {
		return {			
			jobs: 
				[
					{ title: 'Web Developer', id: 1, company: 'The Net Ninja' },
					{ title: 'Web Designer', id: 2, company: 'Codevolution' },
					{ title: 'Android Developer', id: 3, company: 'Vuemastry' }
				]
			}
	}
}
</script>

<style>
	h1{
		color: limegreen;
	}
	.jobs{
		background-color: #eee;
		width: 75%;
		margin: 20px auto;
		padding: 15px;
		border-radius: 5px;
		cursor: pointer;

	}
	.jobs:hover{
		background-color: #ccc;
	}
	a{
		text-decoration: none;
		color: 	crimson;
	}
</style>