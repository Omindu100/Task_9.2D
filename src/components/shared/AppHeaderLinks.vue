<script>
export default {
	props: ['showModal', 'isOpen'],
};
</script>

<template>
	<!-- Header links -->
	<div
		:class="isOpen ? 'block' : 'hidden'"
		class="header_list"
	>
		<router-link
			to="/projects"
			class="router "
			aria-label="Projects"
			>Projects</router-link
		>
		<router-link
			to="/about"
			class="router"
			aria-label="About Me"
			>About Me</router-link
		>
		<router-link
			to="/contact"
			class="router"
			aria-label="Contact"
			>Contact</router-link
		>
		<div
		>
			<button
				@click="showModal()"
				aria-label="Hire Me Button"
			>
			</button>
		</div>
	</div>
</template>

<style scoped>
.router{
	display: block; 
padding-top: 0.75rem; 
margin-bottom: 0.5rem; 
border-top-width: 2px; 
font-size: 1.125rem;
line-height: 1.75rem; 
font-weight: 540; 
text-align: left; 
color: rgb(49, 44, 44);
}

@media (min-width: 640px) { 
.router{
		padding-top: 0.5rem;
padding-bottom: 0.5rem; 
padding-top: 0.5rem; 
margin-left: 1rem;
margin-right: 1rem; 
border-top-width: 0; 
	}
	.header_list{
		display: flex; 
	padding: 0; 
	margin-top: 0.75rem; 
	margin-left: 1rem; 
	box-shadow: none; 
	}
 }
 .router:hover {
 color: #3d29a1; 
 }
.header_list{
	padding: 1.25rem; 
	padding-left: 10%;
	padding-right: 10%;
	margin: 0; 
	margin-top: 1.25rem; 
	justify-content: center; 
	align-items: center; 
}


</style>
