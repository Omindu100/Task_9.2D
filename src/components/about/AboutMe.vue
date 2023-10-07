<script>
export default {
	setup() {
		return {
			bios: [
				{
					id: 1,
					title:"About Me: Omindu Weragodage",
					bio:
						'Hello! I am Omindu Weragodage, a passionate software developer with a deep love for creating elegant and efficient solutions to complex problems. I thrive in the dynamic and ever-evolving world of technology, where creativity meets functionality.',
				},
				{
					id: 2,
					title:"Background:",
					bio:
						'I embarked on my journey in the realm of software development with a burning curiosity to explore the endless possibilities of code. My academic background in computer science laid the foundation, but it was my insatiable thirst for knowledge and hands-on experience that truly shaped me into the developer I am today.',
				},
				{
					id: 3,
					title:"Experience:",
					bio:
						'My technical skill set encompasses a wide range of programming languages, including but not limited to Python, Java and JavaScript. I have a knack for crafting robust and scalable applications, with a keen eye for detail and a passion for writing clean, maintainable code.',
				},
				{
					id: 4,
					title:"",
					bio:
						'Thank you for taking the time to get to know me a little better. I am excited about the future of technology and the endless possibilities it holds, and I look forward to being a part of it every step of the way.',
				},
			],
		};
	},
};
</script>

<template>
	<div class="aboutme">
		<!-- About profile image -->
		<div class="prof_img">
			<img
				src="@/assets/images/profile1.jpg"
				class="img"
				alt=""
			/>
		</div>

		<!-- About details -->
		<div class="detail" >
			<div v-for="bio in bios"
				:key="bio.id">
			<strong class="about_heading"> {{ bio.title }}</strong>	
			<p
				
				class="about_detail"
			>
				{{ bio.bio }}
			</p>
		</div>	
		</div>
	</div>
</template>

<style scoped>
.prof_img{
	margin-bottom: 1.75rem; 
	width: 100%; 
 }
 @media (min-width: 640px) { 
 .prof_img{
	margin-bottom: 0; 
	width: 25%;
 } }
 .about_heading{
	font-size: larger;
	margin-bottom: 1rem;
 }

.about_detail{
	margin-bottom: 1rem; 
	font-size: 1.125rem;
	line-height: 1.75rem; 
}
.img{
	border-radius: 0.75rem; 
	width: 24rem; 
}
.detail{
	width: 100%; 
	text-align: left; 
}
@media (min-width: 640px) { 
	.detail{
		width: 75%; 
	}
 }
.aboutme{
	display: block; 
	margin-top: 2.5rem; 
}


@media (min-width: 640px) { 
	.aboutme{
		display: flex; 
		margin-top: 5rem; 
		gap: 2.5rem; 
	}
 }
</style>