<script>
import feather from 'feather-icons';
import FooterCopyright from './FooterCopyright.vue';
import { socialLinks } from '../../data/socialLinks';

export default {
	components: { FooterCopyright },
	data() {
		return {
			socials: socialLinks,
		};
	},
	mounted() {
		feather.replace();
	},
	updated() {
		feather.replace();
	},
};
</script>

<template>
	<div class="">
		<div
			class="footer"
		>
			<!-- Footer social links -->
			<div
				class="footer_section"
			>
				<p
					class="footer_heading"
				>
					Follow me
				</p>
				<ul class="footer_icon_section">
					<a
						v-for="social in socials"
						:key="social.id"
						:href="social.url"
						target="__blank"
						class="footer_icon"
					>
						<i
							:data-feather="social.icon"
							class="social_icon"
						></i>
					</a>
				</ul>
			</div>

			<!-- Footer copyright -->
			<FooterCopyright />
		</div>
	</div>
</template>

<style scoped>

.footer{
	padding-bottom: 2rem; 
	padding-top: 5rem; 
	margin-top: 5rem; 
	border-top-width: 2px; 
}


.footer_section{
	display: flex; 
margin-bottom: 3rem; 
flex-direction: column; 
justify-content: center; 
align-items: center; 

}

.footer_heading{
	margin-bottom: 1.25rem; 
	font-size: 1.875rem;
	line-height: 2.25rem; 
	font-weight: 600; 
}
.footer_icon_section{
	display: flex; 
	gap: 1rem; 
}
.footer_icon{
	padding: 1rem; 
	border-radius: 0.5rem; 
	color: #9CA3AF; 
	background-color: #F9FAFB; 
	transition-duration: 500ms; 
	cursor: pointer; 
	box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05); 

}
.footer_icon:hover {
 color: #6366F1; 
	background-color: #F3F4F6; 
 }

.social_icon{
	width: 1.25rem; 
	height: 1.25rem; 
 }

@media (min-width: 640px) { 
 .footer_section{	
  margin-bottom: 5rem; 
 }

 .footer_heading{
	font-size: 2.25rem;
line-height: 2.5rem;
color:rgb(21, 36, 36); 
 }

 .footer_icon_section{
	gap: 2rem; 
}

.social_icon{
	width: 2rem; 
	height: 2rem;  
 }

}


</style>
