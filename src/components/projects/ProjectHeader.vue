<script>
export default {
	props: ['singleProjectHeader'],
};
</script>

<template>
	<div>
		<!-- Project heading and meta info -->
		<p
			class="info"
		>
			{{ singleProjectHeader.singleProjectTitle }}
		</p>
		<div class="flex">
			<div class="flex">
				<i
					data-feather="clock"
					class="clock_tag"
				></i>
				<span
					class="c_t"
					>{{ singleProjectHeader.singleProjectDate }}</span
				>
			</div>
			<div class="flex">
				<i
					data-feather="tag"
					class="clock_tag"
				></i>
				<span
					class="c_t"
					>{{ singleProjectHeader.singleProjectTag }}</span
				>
			</div>
		</div>
	</div>
</template>
<style scoped>
.info{
	margin-bottom: 1.75rem; 
	margin-top: 3.5rem; 
	font-size: 1.875rem;
	line-height: 2.25rem; 
	font-weight: 700; 
	text-align: left; 
}
@media (min-width: 640px) { 
	.info{  
		margin-top: 5rem; 
		font-size: 2.25rem;
		line-height: 2.5rem; 
	}

 }
 .clock_tag{
	width: 1rem; 
	height: 1rem; 
 }
 .c_t{
	margin-left: 0.5rem; 
	line-height: 1; 
 }
</style> 
