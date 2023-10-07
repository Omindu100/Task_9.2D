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
				singleProjectTitle: 'Hospital Management System',
				singleProjectDate: 'Feb 26, 2022',
				singleProjectTag: 'Web app',
			},
			projectImages: [
				{
					id: 1,
					title: 'Hospital Management System',
					img: require('@/assets/images/project-11.jpg'),
				},
				{
					id: 2,
					title: 'Hospital Management System',
					img: require('@/assets/images/project-12.jpg'),
				},
				{
					id: 3,
					title: 'Hospital Management System',
					img: require('@/assets/images/project-13.jpg'),
				},
			],
			projectInfo: {
				clientHeading: 'About Client',
				companyInfos: [
					{
						id: 1,
						title: 'Name',
						details: 'City general hospital',
					},
					{
						id: 2,
						title: 'Services',
						details: 'Software Development',
					},
					{
						id: 3,
						title: 'Website',
						details: 'N/A',
					},
					{
						id: 4,
						title: 'Phone',
						details: '+1-987-654-3210',
					},
				],
				objectivesHeading: 'Objective',
				objectivesDetails:
					'Develop a comprehensive Hospital Management System to streamline patient records, appointments, and billing processes. Enhance the efficiency of hospital operations.',
				technologies: [
					{
						title: 'Tools & Technologies',
						techs: [
							'HTML',
							'CSS',
							'JavaScript',
							'Java',
							'MySQL',
						],
					},
				],
				projectDetailsHeading: 'Challenge',
				projectDetails: [
					{
						id: 1,
						details:
							'The Hospital Management System project improved the overall operations of City General Hospital by digitizing and automating various administrative and clinical processes. Patient care and management became more efficient, leading to increased patient satisfaction.',
					},
					{
						id: 2,
						details:
							' Protecting sensitive patient data from breaches or unauthorized access was paramount. Compliance with HIPAA regulations and implementing strong data encryption measures required extensive planning and execution.',
					},
					{
						id: 3,
						details:
							' Integrating the new Hospital Management System with existing legacy systems posed compatibility and data migration challenges. Ensuring seamless communication between different systems while maintaining data integrity was a complex task.',
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
						title: 'Mobile Banking App',
						img: require('@/assets/images/project-21.jpg'),
					},
					{
						id: 2,
						title: 'Online Learning platform',
						img: require('@/assets/images/project-51.png'),
					},
					{
						id: 3,
						title: 'Inventory Management System',
						img: require('@/assets/images/project-31.jpg'),
					},
					{
						id: 4,
						title: 'Customer Relationship Management (CRM) Software',
						img: require('@/assets/images/project-41.png'),
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
