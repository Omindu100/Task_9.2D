<script>
export default {
	props: ['projectImages'],
};
</script>

<template>
	<div class="project_gallery">
		<div
			v-for="projectImage in projectImages"
			:key="projectImage.id"
		>
			<img
				:src="projectImage.img"
				class="img"
				alt="{{ projectImage.title }}"
			/>
		</div>
	</div>
</template>
<style scoped>
.project_gallery{
	display: grid ;
	margin-top: 3rem; 
	grid-template-columns: repeat(1, minmax(0, 1fr)); 
 }
 @media (min-width: 640px) { 
	.project_gallery{
		grid-template-columns: repeat(3, minmax(0, 1fr)); 
		gap: 2.5rem; }
}
.img{
	border-radius: 0.75rem; 
	cursor: pointer; 
	box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05); 
}

@media (min-width: 640px) { 
	.img{
		box-shadow: none; 
	}
 }
</style>