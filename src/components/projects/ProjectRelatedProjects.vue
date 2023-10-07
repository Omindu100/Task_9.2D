<script>
export default {
	props: ['relatedProject'],
};
</script>

<template>
	<div
		class="prp"
	>
		<p
			class="related_project"
		>
			{{ relatedProject.relatedProjectsHeading }}
		</p>

		<div class="list">
			<div v-for="item in relatedProject.relatedProjects" :key="item.id">
				<img
					:src="item.img"
					class="image"
					:alt="item.title"
				/>
			</div>
		</div>
	</div>
</template>
<style scoped>
.prp{
	padding-top: 2.5rem; 
	margin-top: 2.5rem; 
	border-top-width: 2px; 
}

@media (min-width: 640px) { 
	.prp{
		padding-top: 3.5rem; 
		margin-top: 5rem; 
	}
 }

 .related_project{
	margin-bottom: 2.5rem; 
	font-size: 1.875rem;
	line-height: 2.25rem; 
	font-weight: 700; 
	text-align: left; 
 }
@media (min-width: 640px) { 
	.related_project{
		margin-bottom: 3.5rem; 
	}
 }
.list{
	display: grid;
	grid-template-columns: repeat(1, minmax(0, 1fr)); 
	gap: 2.5rem; 
}

@media (min-width: 640px) { 
	.list{
		grid-template-columns: repeat(4, minmax(0, 1fr)); 
	}
 }
.image{
	border-radius: 0.75rem; 
	cursor: pointer; 
}
</style>
