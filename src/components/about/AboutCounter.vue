<script>
import counter from 'vue3-autocounter';
export default {
	components: {
		counter,
	},
	data: () => {
		return {
			experienceTitle: 'Years of experience',
			ongoingTitle: 'Ongoing Projects',
			feedbackTitle: 'Positive feedback',
			projectsTitle: 'Projects completed',
		};
	},
};
</script>

<template>
	<div class="aboutcounter">
		<!-- About me counters -->
		<div
			class="exp"
		>
			<!-- Years of experience counter -->
			<div class="expe_cou">
				<counter
					ref="counter"
					:startAmount="0"
					:endAmount="2"
					:duration="1"
					:autoinit="true"
					@finished="alert(`Counting finished!`)"
					class="counter"
					aria-label="About Status Counter"
				/>
				<span
					class="block"
				>
					{{ experienceTitle }}
				</span>
			</div>

			<!-- GitHub stars counter -->
			<div class="expe_cou">
				<counter
					ref="counter"
					:startAmount="0"
					:endAmount="1"
					:duration="1"
					:autoinit="true"
					@finished="alert(`Counting finished!`)"
					class="counter"
				/>
				<span
					class="block"
					>{{ ongoingTitle }}</span
				>
			</div>

			<!-- Positive feedback counter -->
			<div class="expe_cou">
				<counter
					ref="counter"
					:startAmount="0"
					:endAmount="90"
					:duration="1"
					suffix="%"
					:autoinit="true"
					@finished="alert(`Counting finished!`)"
					class="counter"
				/>
				<span
					class="block"
				>
					{{ feedbackTitle }}
				</span>
			</div>

			<!-- Projects completed counter -->
			<div class="expe_cou">
				<counter
					ref="counter"
					:startAmount="0"
					:endAmount="7"
					:duration="1"
					:autoinit="true"
					@finished="alert(`Counting finished!`)"
					class="counter"
				/>
				<span
					class="block"
				>
					{{ projectsTitle }}
				</span>
			</div>
		</div>
	</div>
</template>

<style scoped>
.aboutcounter{
	margin-top: 2.5rem; 
box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05); 
margin-left: 2rem;
margin-right: 2rem;
}

@media (min-width: 640px) { 
.aboutme{  margin-top: 5rem; }
 }

.exp{
display: block; 
padding-top: 5rem;
padding-bottom: 5rem; 
margin: 2rem;
}

@media (min-width: 640px) { 
	.exp{
		display: flex; 
		justify-content: space-between; 
		align-items: center;
	} 
}

.counter{
	margin-bottom: 0.5rem; 
	font-size: 2.25rem;
	line-height: 2.5rem; 
	font-weight: 700; 
}

.expe_cou{
	margin-bottom: 5rem; 
}

@media (min-width: 640px) { 
	.expe_cou{ margin-bottom: 0; }
 }

 .block{
	display: block; 
 }
</style>