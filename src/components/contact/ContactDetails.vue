<script>
export default {
	props: ['contacts'],
};
</script>

<template>
	<div class="contact_detail">
		<div class="detail">
			<h2
				class="header"
			>
				Contact details
			</h2>
			<ul class="font">
				<li class="detail_list" v-for="contact in contacts" :key="contact.id">
					<i
						:data-feather="contact.icon"
						class="list"
					></i>
					<a
						href="#"
						class="link"
						:class="
							contact.icon === 'mail' || contact.icon === 'phone'
								? 'hover'
								: ''
						"
						aria-label="Website and Phone"
					>
						{{ contact.name }}
					</a>
				</li>
			</ul>
		</div>
	</div>
</template>

<style scoped>
.detail{
    padding-left: 1.5rem;
    padding-right: 1.5rem; 
    max-width: 36rem; 
    text-align: left; 
}
.header{
    margin-bottom: 2rem; 
    margin-top: 3rem; 
    font-size: 1.5rem;
    line-height: 2rem; 
}
.detail_list{
	display: flex; 
}
.list{
	margin-right: 1rem; 
	width: 1.25rem; 
	color: #6B7280; 
}
.email{
	margin-bottom: 1rem; 
	font-size: 1.125rem;
	line-height: 1.75rem; 
}
.contact_detail{
	width: 100%; 
}

@media (min-width: 768px) { 
	.contact_detail{
		width: 50%; 
	}

 }
 .link{
	margin-bottom: 1rem; 
	font-size: 1.125rem;
	line-height: 1.75rem; 
 }
 .hover{
	cursor: pointer; 
 }
.hover:hover {
 text-decoration: underline; 
 }
 .font{
	font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
	color: #262523;
 }
</style>
