<script>
import feather from 'feather-icons';

export default {
	props: ['projectInfo'],

	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
};
</script>

<template>
	<div class="section">
		<!-- Single project left section details -->
		<div class="left_section">
			<!-- Single project client details -->
			<div class="client">
				<p
					class="title"
				>
					{{ projectInfo.clientHeading }}
				</p>
				<ul class="leading-loose">
					<li
						v-for="info in projectInfo.companyInfos"
						:key="info"
						class="detail"
					>
						<span>{{ info.title }}: </span>
						<a
							href="#"
							aria-label="Project Website and Phone"
							>{{ info.details }}</a
						>
					</li>
				</ul>
			</div>

			<!-- Single project objectives -->
			<div class="objective">
				<p
					class="title"
				>
					{{ projectInfo.objectivesHeading }}
				</p>
				<p
					class="detail"
				>
					{{ projectInfo.objectivesDetails }}
				</p>
			</div>

			<!-- Single project technologies -->
			<div class="objective">
				<p
					class="title"
				>
					{{ projectInfo.technologies[0].title }}
				</p>
				<p
					class="detail"
				>
					{{ projectInfo.technologies[0].techs.join(', ') }}
				</p>
			</div>

			<!-- Single project social sharing -->
			<div>
				<p
					class="title"
				>
					{{ projectInfo.socialSharingsHeading }}
				</p>
				<div class="social_icon">
					<a
						v-for="social in projectInfo.socialSharings"
						:key="social.id"
						:href="social.url"
						target="__blank"
						aria-label="Share Project"
						class="media_icon"
						><i
							:data-feather="social.icon"
							class="media_icon_i"
						></i
					></a>
				</div>
			</div>
		</div>

		<!-- Single project right section details -->
		<div class="right_section">
			<p
				class="right_heading"
			>
				{{ projectInfo.projectDetailsHeading }}
			</p>
			<p
				v-for="projectDetail in projectInfo.projectDetails"
				:key="projectDetail.id"
				class="right_detail">
				{{ projectDetail.details }}
			</p>
		</div>
	</div>
</template>
<style scoped>
.section{
	display: block; 
	margin-top: 3.5rem; 
	gap: 0; 
}

@media (min-width: 640px) { 
	.section{  
		display: flex; 
		gap: 2.5rem; }
 }

 .title{
	margin-bottom: 0.5rem; 
	font-size: 1.5rem;
	line-height: 2rem; 
	margin-top: 2rem;
 }

 .left_section{
	width: 100%; 
text-align: left; 

@media (min-width: 640px) { 
  width: 33.333333%; 
 }

 }

 .client{
	margin-bottom: 1.75rem; 
 }

 .detail{
	color:gray;
 }

 .social_icon{
	display: flex; 
	margin-top: 1.25rem; 
	gap: 0.75rem; 
	align-items: center; 

 }

 .media_icon{
	padding: 0.5rem; 
border-radius: 0.5rem; 
color: #9CA3AF; 
transition-duration: 500ms; 
box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05); 

	:hover {
		color: #000000; 
  }
 }

 .media_icon_i{
	width: 1rem; 
	height: 1rem; 
	
 }

@media (min-width: 1024px) { 
	.media_icon_i{
		width: 1.25rem; 
	height: 1.25rem; 
	}

 }

.right_section{
	margin-top: 2.5rem; 
	width: 100%; 
	text-align: left; 

@media (min-width: 640px) { 
  margin-top: 0; 
width: 66.666667%; 
 }


}

.right_heading{
	margin-bottom: 1.75rem; 
	font-size: 1.5rem;
	line-height: 2rem; 
	font-weight: 700; 
}

.right_detail{
	margin-bottom: 1.25rem; 
	font-size: 1.125rem;
	line-height: 1.75rem; 
	color:gray;
}
.obejctive{
	margin-bottom: 1.75rem;
	margin-top: 2rem; 
}
</style>