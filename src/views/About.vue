<script>
import AboutMe from '@/components/about/AboutMe';
import AboutCounter from '@/components/about/AboutCounter';
import feather from 'feather-icons';

export default {
	name: 'About',
	components: {
		AboutMe,
		AboutCounter,
	},
	data: () => {
		return {};
	},
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
	methods: {},
};
</script>

<template>
	<div>
		<!-- About me -->
		<div class="about_container">
			<AboutMe />
		</div>

		<!-- About counter -->
		<AboutCounter />

		
	</div>
</template>

<style scoped>
/* .about_container{
	margin-left: 2rem;
  margin-right: 2rem;
}

@media (min-width: 640px) {
  .about_container {
    margin-bottom: 2rem;
    margin-right: 2.5rem;
    margin-left: 2.5rem;
  }
} */

.about_container{
	display: flex; 
	padding-top: 1.25rem;
	padding-bottom: 1.25rem; 
	flex-direction: column-reverse; 
	margin-left: 8%;
	margin-right: 8%;
}

@media (min-width: 768px) { 
	.about_container{
		padding-top: 2.5rem;
		padding-bottom: 2.5rem; 
		margin-top: 2.5rem; 
		flex-direction: row;
	} 
 }

</style>
