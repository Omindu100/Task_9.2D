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
				singleProjectTitle: 'Inventory Management System',
				singleProjectDate: 'March 29, 2022',
				singleProjectTag: 'Software Development',
			},
			projectImages: [
				{
					id: 1,
					title: 'Inventory Management System',
					img: require('@/assets/images/project-31.jpg'),
				},
				{
					id: 2,
					title: 'Inventory Management System',
					img: require('@/assets/images/project-32.jpg'),
				},
				{
					id: 3,
					title: 'Inventory Management System',
					img: require('@/assets/images/project-33.jpg'),
				},
			],
			projectInfo: {
				clientHeading: 'About Client',
				companyInfos: [
					{
						id: 1,
						title: 'Name',
						details: 'ABC Retailers',
					},
					{
						id: 2,
						title: 'Services',
						details: 'Custom Software Development',
					},
					{
						id: 3,
						title: 'Website',
						details: 'N/A',
					},
					{
						id: 4,
						title: 'Phone',
						details: '+1-555-789-1234',
					},
				],
				objectivesHeading: 'Objective',
				objectivesDetails:
					'Develop an Inventory Management System to track and manage the stock levels, sales, and reorder points for ABC Retailers\' stores.',
				technologies: [
					{
						title: 'Tools & Technologies',
						techs: [
							'Angular',
							'Python',
							'PostgreSQL',
						],
					},
				],
				projectDetailsHeading: 'Challenge',
				projectDetails: [
					{
						id: 1,
						details:
							'Providing real-time stock updates and syncing data across multiple stores while minimizing delays presented a technical challenge. Accurate inventory information was crucial for optimizing stock levels.',
					},
					{
						id: 2,
						details:
							'Maintaining data accuracy and reliability throughout the system\'s lifespan was a continuous challenge. Data discrepancies could lead to inventory mismanagement and financial losses.',
					},
					{
						id: 3,
						details:
							'The Inventory Management System project streamlined ABC Retailers\' operations by providing real-time insights into inventory levels and sales trends. It resulted in improved stock management and reduced overstocking or understocking issues.',
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
						title: 'CRM Software',
						img: require('@/assets/images/project-41.png'),
					},
					{
						id: 2,
						title: 'Mobile Banking App',
						img: require('@/assets/images/project-21.jpg'),
					},
					{
						id: 1,
						title: 'Hospital Management System',
						img: require('@/assets/images/project-61.png'),
					},
					
					{
						id: 4,
						title: 'Online Learning Platform',
						img: require('@/assets/images/project-51.png'),
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
