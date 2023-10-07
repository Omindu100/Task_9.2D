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
				singleProjectTitle: 'Online Shopping Platform',
				singleProjectDate: 'Feb 26, 2022',
				singleProjectTag: 'Web app',
			},
			projectImages: [
				{
					id: 1,
					title: 'Online Shopping Platform',
					img: require('@/assets/images/project-61.png'),
				},
				{
					id: 2,
					title: 'Online Shopping Platform',
					img: require('@/assets/images/project-62.png'),
				},
				{
					id: 3,
					title: 'Online Shopping Platform',
					img: require('@/assets/images/project-63.png'),
				},
			],
			projectInfo: {
				clientHeading: 'About Client',
				companyInfos: [
					{
						id: 1,
						title: 'Name',
						details: 'Telco Company Ltd',
					},
					{
						id: 2,
						title: 'Services',
						details: 'Web Development',
					},
					{
						id: 3,
						title: 'Website',
						details: 'https://telco.com',
					},
					{
						id: 4,
						title: 'Phone',
						details: '+1-123-456-7890',
					},
				],
				objectivesHeading: 'Objective',
				objectivesDetails:
					'Create a user-friendly e-commerce website for ABC Electronics to showcase and sell their products online. Increase online sales and customer engagement.',
				technologies: [
					{
						title: 'Tools & Technologies',
						techs: [
							'HTML',
							'CSS',
							'JavaScript',
							'PHP',
							'MySQL',
						],
					},
				],
				projectDetailsHeading: 'Challenge',
				projectDetails: [
					{
						id: 1,
						details:
							'Ensuring the secure integration of payment gateways posed a challenge due to the need for robust encryption, fraud prevention measures, and compliance with payment industry standards like PCI DSS. Any security vulnerabilities could lead to financial losses and data breaches.',
					},
					{
						id: 2,
						details:
							'The website\'s success led to high traffic volumes, requiring meticulous optimization to maintain fast load times and smooth user experiences. Balancing performance with scalability was crucial to prevent server overload during peak shopping seasons.',
					},
					{
						id: 3,
						details:
							'The Online Shopping Platform project aimed to help ABC Electronics establish an online presence. The platform allows customers to browse and purchase electronic products with ease. The project successfully increased online sales and improved customer satisfaction.',
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
