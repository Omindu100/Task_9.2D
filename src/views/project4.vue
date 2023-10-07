<script>
import feather from 'feather-icons';
import ProjectHeader from '../components/projects/ProjectHeader.vue';
import ProjectGallery from '../components/projects/ProjectGallery.vue';
import ProjectInfo from '../components/projects/ProjectInfo.vue';
import ProjectRelatedProjects from '../components/projects/ProjectRelatedProjects.vue';

export default {
	name: 'Projects',
	components: {
		ProjectHeader,
		ProjectGallery,
		ProjectInfo,
		ProjectRelatedProjects,
	},
	data: () => {
		return {
			singleProjectHeader: {
				singleProjectTitle: 'Customer Relationship Management (CRM) Software',
				singleProjectDate: 'Apr 02, 2023',
				singleProjectTag: 'CRM Software',
			},
			projectImages: [
				{
					id: 1,
					title: 'Customer Relationship Management (CRM) Software',
					img: require('@/assets/images/project-41.png'),
				},
				{
					id: 2,
					title: 'Customer Relationship Management (CRM) Software',
					img: require('@/assets/images/project-42.png'),
				},
				{
					id: 3,
					title: 'Customer Relationship Management (CRM) Software',
					img: require('@/assets/images/project-43.jpg'),
				},
			],
			projectInfo: {
				clientHeading: 'About Client',
				companyInfos: [
					{
						id: 1,
						title: 'Name',
						details: 'Selica Enterprises',
					},
					{
						id: 2,
						title: 'Services',
						details: 'CRM Software Development',
					},
					{
						id: 3,
						title: 'Website',
						details: 'https://selicaent.com',
					},
					{
						id: 4,
						title: 'Phone',
						details: '+1-888-555-4321',
					},
				],
				objectivesHeading: 'Objective',
				objectivesDetails:
					'Create a customized CRM software solution to help XYZ Enterprises manage customer interactions, sales leads, and marketing campaigns efficiently.',
				technologies: [
					{
						title: 'Tools & Technologies',
						techs: [
							'React',
							'Ruby',
							'PostgreSQL',
						],
					},
				],
				projectDetailsHeading: 'Challenge',
				projectDetails: [
					{
						id: 1,
						details:
							'The CRM Software project transformed Selica Enterprises\' customer management processes, enhancing their ability to nurture leads and build strong customer relationships. The software allowed them to track customer interactions and streamline sales and marketing efforts.',
					},
					{
						id: 2,
						details:
							'Customizing the CRM to align with XYZ Enterprises\' specific business processes and requirements was a complex endeavor. It required detailed understanding of the company\'s operations and careful software configuration.',
					},
					{
						id: 3,
						details:
							'Migrating data from existing CRM and other legacy systems to the new solution without data loss or corruption demanded thorough planning and robust data migration tools.',
					},
				
				],
				socialSharingsHeading: 'Share This',
				socialSharings: [
					{
						id: 1,
						name: 'Twitter',
						icon: 'twitter',
						url: '#',
					},
					
					{
						id: 2,
						name: 'Facebook',
						icon: 'facebook',
						url: '#',
					},
					{
						id: 3,
						name: 'LinkedIn',
						icon: 'linkedin',
						url: '#',
					},
					
				],
			},
			relatedProject: {
				relatedProjectsHeading: 'Related Projects',
				relatedProjects: [
					{
						id: 1,
						title: 'Hospital Management System',
						img: require('@/assets/images/project-11.jpg'),
					},
					{
						id: 2,
						title: 'Mobile Banking App',
						img: require('@/assets/images/project-21.jpg'),
					},
					{
						id: 3,
						title: 'Inventory Management System',
						img: require('@/assets/images/project-31.jpg'),
					},
					{
						id: 4,
						title: 'Online Shopping platform',
						img: require('@/assets/images/project-61.png'),
					},
				],
			},
		};
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
	<div class=" header">
		<!-- Project header -->
		<ProjectHeader :singleProjectHeader="singleProjectHeader" />

		<!-- Project gallery -->
		<ProjectGallery :projectImages="projectImages" />

		<!-- Project information -->
		<ProjectInfo :projectInfo="projectInfo" />

		<!-- Project related projects -->
		<ProjectRelatedProjects :relatedProject="relatedProject" />
	</div>
</template>

<style scoped>
.header{
	display:block;
	margin-bottom:0.5rem;
	font-size:1.125rem;
	line-height:1.75rem;
	font-weight:500;
	text-align:left;
}
	@media (min-width: 640px){
		.header{	
		padding-top:0.5rem;
		padding-bottom:0.5rem;
		margin-left:5%;
		margin-right:5%;
	}
}

</style>
