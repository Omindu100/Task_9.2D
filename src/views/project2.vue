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
				singleProjectTitle: 'Mobile Banking App',
				singleProjectDate: 'Feb 26, 2022',
				singleProjectTag: 'Mobile app',
			},
			projectImages: [
				{
					id: 1,
					title: 'Mobile Banking App',
					img: require('@/assets/images/project-21.jpg'),
				},
				{
					id: 2,
					title: 'Mobile Banking App',
					img: require('@/assets/images/project-22.jpg'),
				},
				{
					id: 3,
					title: 'Mobile Banking App',
					img: require('@/assets/images/project-23.jpg'),
				},
			],
			projectInfo: {
				clientHeading: 'About Client',
				companyInfos: [
					{
						id: 1,
						title: 'Name',
						details: 'RDB Bank',
					},
					{
						id: 2,
						title: 'Services',
						details: 'Mobile Development',
					},
					{
						id: 3,
						title: 'Website',
						details: 'https://rdb.com',
					},
					{
						id: 4,
						title: 'Phone',
						details: '+1-800-123-4567',
					},
				],
				objectivesHeading: 'Objective',
				objectivesDetails:
					'Create a user-friendly mobile banking app for XYZ Bank\'s customers, enabling them to perform transactions, check balances, and access account information on their smartphones.',
				technologies: [
					{
						title: 'Tools & Technologies',
						techs: [
							'React Native',
							'Node JS',
							'Mongo DB',
							
						],
					},
				],
				projectDetailsHeading: 'Challenge',
				projectDetails: [
					{
						id: 1,
						details:
							' Ensuring the security of financial transactions was a top concern. Implementing encryption, multi-factor authentication, and continuous monitoring to detect and prevent fraudulent activities was a critical challenge.',
					},
					{
						id: 2,
						details:
							'The app needed to work flawlessly on various mobile devices and operating systems. Designing a responsive and cross-platform user interface while providing consistent functionality across devices required careful planning.',
					},
					{
						id: 3,
						details:
							'The Mobile Banking App project provided RDB Bank\'s customers with a convenient and secure way to manage their accounts on-the-go. The app has received positive feedback for its ease of use and functionality.',
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
						title: 'Online Shopping Platform',
						img: require('@/assets/images/project-61.png'),
					},
					{
						id: 2,
						title: 'Hospital Management System',
						img: require('@/assets/images/project-13.jpg'),
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
