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
				singleProjectTitle: 'Online Learning Platform',
				singleProjectDate: 'Feb 30, 2023',
				singleProjectTag: 'Web app',
			},
			projectImages: [
				{
					id: 1,
					title: 'Online Learning Platform',
					img: require('@/assets/images/project-51.png'),
				},
				{
					id: 2,
					title: 'Online Learning Platform',
					img: require('@/assets/images/project-52.png'),
				},
				{
					id: 3,
					title: 'Online Learning Platform',
					img: require('@/assets/images/project-53.png'),
				},
			],
			projectInfo: {
				clientHeading: 'About Client',
				companyInfos: [
					{
						id: 1,
						title: 'Name',
						details: 'Edu tech Academy',
					},
					{
						id: 2,
						title: 'Services',
						details: 'E-learning Platform Development',
					},
					{
						id: 3,
						title: 'Website',
						details: 'https://edutechacademy.com',
					},
					{
						id: 4,
						title: 'Phone',
						details: '+1-777-987-6543',
					},
				],
				objectivesHeading: 'Objective',
				objectivesDetails:
					'Develop an online learning platform with features like video lectures, quizzes, and student progress tracking for EduTech Academy to offer courses and educational content.',
				technologies: [
					{
						title: 'Tools & Technologies',
						techs: [
							'Vue js',
							'Django',
							'MySQL',
						],
					},
				],
				projectDetailsHeading: 'Challenge',
				projectDetails: [
					{
						id: 1,
						details:
							'The Online Learning Platform project empowered EduTech Academy to reach a wider audience with their educational content. Students can access courses, track their progress, and interact with instructors through the platform, enhancing the learning experience.',
					},
					{
						id: 2,
						details:
							'The platform experienced rapid user growth, necessitating constant infrastructure scaling to accommodate the increasing load. Ensuring that the platform remained responsive and reliable was a significant challenge.',
					},
					{
						id: 3,
						details:
							'Protecting educational content from unauthorized access and piracy was vital. Implementing digital rights management (DRM) and content encryption solutions posed technical and legal challenges.',
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
