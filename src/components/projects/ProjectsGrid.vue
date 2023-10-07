<script>
import feather from 'feather-icons';
import ProjectsFilter from './ProjectsFilter.vue';
import ProjectSingle from './ProjectSingle.vue';
import projects from '../../data/projects';

export default {
	components: { ProjectSingle, ProjectsFilter },
	data: () => {
		return {
			projects,
			projectsHeading: 'Projects Portfolio',
			selectedCategory: '',
			searchProject: '',
		};
	},
	computed: {
		// Get the filtered projects
		filteredProjects() {
			if (this.selectedCategory) {
				return this.filterProjectsByCategory();
			} else if (this.searchProject) {
				return this.filterProjectsBySearch();
			}
			return this.projects;
		},
	},
	methods: {
		// Filter projects by category
		filterProjectsByCategory() {
			return this.projects.filter((item) => {
				let category =
					item.category.charAt(0).toUpperCase() +
					item.category.slice(1);
				console.log(category);
				return category.includes(this.selectedCategory);
			});
		},
		// Filter projects by title search
		filterProjectsBySearch() {
			let project = new RegExp(this.searchProject, 'i');
			return this.projects.filter((el) => el.title.match(project));
		},
	},
	mounted() {
		feather.replace();
	},
};
</script>

<template>
	<!-- Projects grid -->
	<section class="project_grid">
		<!-- Projects grid title -->
		<div class="">
			<p
				class="grid_title"
			>
				{{ projectsHeading }}
			</p>
		</div>

		<!-- Filter and search projects -->
		<div class="grid_container">
			<h3
				class="search_title"
			>
				Search projects by title or filter by category
			</h3>
			<div
				class="search_box_container">
				<div class="search_box">
					<span
						class="search">
						<i
							data-feather="search"
							class="search_icon"
						></i>
					</span>
					<input
						v-model="searchProject"
						class="search_input"
						id="name"
						name="name"
						type="search"
						required=""
						placeholder="Search Projects"
						aria-label="Name"
					/>
				</div>
				<ProjectsFilter @filter="selectedCategory = $event" />
			</div>
		</div>

		<!-- Projects grid -->
		<div
			class="grid"
		>
			<ProjectSingle
				v-for="project in filteredProjects"
				:key="project.id"
				:project="project"
			/>
		</div>
	</section>
</template>

<style scoped>
.project_grid{
	padding-top: 2.5rem; 
	margin-left: 8%;
	margin-right: 8%;
	
}
@media (min-width: 640px) { 
	.project_grid{
		padding-top: 3.5rem;
	}  
 }
 .grid_title{
	margin-bottom: 0.5rem; 
	font-size: 1.5rem;
	line-height: 2rem; 
	font-weight: 600; 
 }
 @media (min-width: 640px) {
	.grid_title{
		font-size: 3rem;
		line-height: 1; 
	}
  }

 .grid_container{
	margin-top: 2.5rem; 
 }
 @media (min-width: 640px) { 
  .grid_container{
	margin-top: 2.5rem; 
  }
 }

 .search_title{
	margin-bottom: 1rem; 
	font-weight: 400; 
	font-size: larger;
	text-align: center; 
 }

 .search{
	padding: 0.625rem; 
	border-radius: 0.75rem; 
	cursor: pointer; 
	box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05); 
 }

.search_box_container{
	display: flex; 
	padding-bottom: 0.75rem; 
	gap: 0.5rem; 
	justify-content: space-between; 
	border-bottom-width: 1px; 

}

.search_box{
	display: flex; 
	gap: 0.5rem; 
	justify-content: space-between; 

}

.search_input{
	padding-top: 0.5rem;
padding-bottom: 0.5rem; 
padding-right: 0.25rem; 
padding-left: 0.75rem; 
border-radius: 0.5rem; 
border-color: #E5E7EB; 
font-size: 0.875rem;
line-height: 1.25rem; 
}

.grid{
	display: grid ;
	margin-top: 1.5rem; 
	grid-template-columns: repeat(1, minmax(0, 1fr)); 
}

@media (min-width: 640px) { 
	.grid{
		grid-template-columns: repeat(2, minmax(0, 1fr)); 
		gap: 2.5rem; 
	}
  
 }

@media (min-width: 1024px) { 
.grid{	
  grid-template-columns: repeat(3, minmax(0, 1fr)); 
 }
}
</style>
