<script>
export default {
	props: ['project'],
};
</script>

<template>
	<router-link
		:to="'/projects/project'+ project.id"
		class="route"
		aria-label="Single Project"
	>
		<div>
			<img
				:src="project.img"
				:alt="project.title"
				class="img"
			/>
		</div>
		<div class="div">
			<p
				class="des"
			>
				{{ project.title }}
			</p>
			<span
				class="span"
				>{{ project.category }}</span
			>
		</div>
	</router-link>
</template>

<style scoped>
.route{
	margin-bottom: 2.5rem; 
	border-radius: 0.75rem; 
	cursor: pointer; 
	box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05); 
}

@media (min-width: 640px) {
	.route{
		margin-bottom: 0; 
	}
}

.route :hover {
 box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04); 
 }

 .img{
	border-top-left-radius: 0.75rem;
	border-top-right-radius: 0.75rem; 
	border-style: none; 
 }

 .des{
	margin-bottom: 0.5rem; 
	font-size: 1.25rem;
	line-height: 1.75rem; 
	font-weight: 600; 
 }

 .span{
	font-size: 1.125rem;
	line-height: 1.75rem; 
}
.div{
	font-size: 1.125rem;
	line-height: 1.75rem; 
}
</style>
