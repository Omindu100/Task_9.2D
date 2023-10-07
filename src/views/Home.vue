<script>
import AppBanner from '@/components/shared/AppBanner';
import ProjectsGrid from '../components/projects/ProjectsGrid.vue';
import Button from '../components/reusable/Button.vue';

export default {
	name: 'Home',
	components: {
		AppBanner,
		ProjectsGrid,
		Button,
	},
};
</script>

<template>
	<div class="appContainer">
		<!-- Banner -->
		<AppBanner class="appBanner" />

		<!-- Projects -->
		<ProjectsGrid />

		<!-- Load more projects button -->
		<div class="loadMore">
			<router-link
				to="/projects"
				class="routerLink"
				aria-label="More Projects"
			>
				<Button title="More Projects" />
			</router-link>
		</div>
	</div>
</template>

<style scoped>


.appContainer {
  display: block;
 
  text-align: center;
  
}
.appBanner{
  margin-left: 8%;
  margin-right: 8%;
}

.appBanner,
.appContainer {
  margin-bottom: 1.25rem;
  
}

@media (min-width: 640px) {
  .appBanner,
  .appContainer {
    margin-bottom: 2rem;
    margin-right: 2.5rem;
    margin-left: 2.5rem;
  }
}

/* Default styles for .loadMore */
.loadMore {
  display: flex;
  margin-top: 2.5rem;
  justify-content: center;
}

/* Responsive styles for screens with a minimum width of 640px */
@media (min-width: 640px) {
  .loadMore {
    margin-top: 5rem;
  }
}

/* Default styles for .routerLink */
.routerLink {
  display: flex;
  padding-top: 0.75rem;
  padding-bottom: 0.75rem;
  padding-left: 1.5rem;
  padding-right: 1.5rem;
  align-items: center;
  border-radius: 0.5rem;
  font-size: 1.125rem;
  line-height: 1.75rem;
  color: #ffffff;
  background-color: #6366F1;
  transition-duration: 300ms;
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

/* Responsive styles for screens with a minimum width of 640px */
@media (min-width: 640px) {
  .routerLink {
    font-size: 1.25rem;
    line-height: 1.75rem;
  }
}

/* Hover styles */
.routerLink:hover {
  background-color: #4F46E5;
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
}


</style>
