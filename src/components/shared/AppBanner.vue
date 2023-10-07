<script>
import feather from 'feather-icons';

export default {
	name: 'Home',
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
	<section
		class="banner_container"
	>
		<!-- Banner left content -->
		<div class="left_section">
			<h1
				class="name_title"
			>
				Omindu Weragodage
			</h1>
			<p
				class="sub_title"
			>
				Web Developer
			</p>
			<div class="download_cv">
				<a
					download="resume.pdf"
					href="/files/resume.pdf"
					class="download_button"
					aria-label="Download Resume"
				>
					<i
						data-feather="arrow-down-circle"
						class="download_icon"
					></i>
					<span
						class="download_text"
						>Download CV</span
					></a
				>
			</div>
		</div>

		<!-- Banner right illustration -->
		<div class="banner_image">
			<img
				src="@/assets/images/developer.svg"
				alt="Developer"
			/>
			
		</div>
	</section>
</template>

<style scoped>
.banner_container{
	display: flex; 
	margin-top: 3rem; 
	flex-direction: column; 
	align-items: center; 
}

.left_section{
	width: 100%; 
	text-align: left; 
}

.name_title{
	font-size: 1.875rem;
	line-height: 2.25rem; 
	text-align: center; 
	text-transform: uppercase;
	font-weight: 800;
	color: #353434; 
}
.sub_title{
	margin-top: 0.5rem; 
	font-size: 1.125rem;
	line-height: 1.75rem; 
	line-height: 1; 
	text-align: center; 
	color: #9CA3AF; 
}
.download_cv{
	display: flex; 
	justify-content: center; 
	color: aqua;
}

.download_button{
	display: flex; 
	padding-top: 0.625rem;
	padding-bottom: 0.625rem; 
	margin-bottom: 1.5rem; 
	margin-top: 3rem; 
	justify-content: center; 
	align-items: center; 
	border-radius: 0.5rem; 
	border-width: 1px; 
	border-color: #C7D2FE; 
	width: 9rem; 
	font-size: 1.125rem;
	line-height: 1.75rem; 
	color: #6B7280; 
	background-color: #EEF2FF; 
	transition-duration: 500ms; 
	box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05); 
	
}
.download_button:hover {
 color: #ffffff; 
 background-color: #6366F1; 
}

.download_icon{
	margin-left: 0; 
	margin-right: 0.5rem; 
	width: 1.25rem; 
	transition-duration: 100ms; 
}

.download_text{
	font-size: 0.875rem;
line-height: 1.25rem; 
transition-duration: 100ms; 
}

.banner_image{
	float: right; 
width: 100%; 
text-align: right; 
}

@media (min-width: 640px) {
.banner_container{
	margin-top: 2.5rem; 
	flex-direction: row; 
	justify-content: space-between; 
}

.name_title{
	text-align: left; 
}

.sub_title{
	font-size: 1.25rem;
	line-height: 1.75rem; 
	text-align: left; 
}

.download_cv{
	display: block; 
}

.download_button{
	padding-top: 0.75rem;
	padding-bottom: 0.75rem; 
	margin-bottom: 0; 
	width: 12rem; 
}
.download_icon{
	margin-left: 0.25rem; 
margin-right: 0.75rem; 
width: 1.5rem; 
}

.download_text{
	font-size: 1.125rem;
line-height: 1.75rem; 
}
}



@media (min-width: 768px) { 
.left_section{
	width: 33.333333%; 
}

.name_title{
	font-size: 1.875rem;
	line-height: 2.25rem; 
}
.banner_image{
	width: 66.666667%; 
}

}

@media (min-width: 1280px) { 
.name_title{
	font-size: 2.25rem;
	line-height: 2.5rem;
}

.sub_title{
	font-size: 1.5rem;
	line-height: 2rem; 
}
}



</style>
