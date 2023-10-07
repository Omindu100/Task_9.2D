<script>
import feather from 'feather-icons';
import ContactForm from '@/components/contact/ContactForm.vue';
import ContactDetails from '@/components/contact/ContactDetails.vue';

export default {
	components: {
		ContactForm,
		ContactDetails,
	},
	data: () => {
		return {
			contacts: [
				{
					id: 1,
					name: 'Cranbourne, Australia',
					icon: 'map-pin',
				},
				{
					id: 2,
					name: 'omindusenarathne@gmail.com',
					icon: 'mail',
				},
				{
					id: 3,
					name: '043 487 4020',
					icon: 'phone',
				},
			],
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
	<div
		class="contact"
	>
		<!-- Contact form -->
		<ContactForm />

		<!-- Contact details -->
		<ContactDetails :contacts="contacts" />
	</div>
</template>

<style>
.contact{
	display: flex; 
	padding-top: 1.25rem;
	padding-bottom: 1.25rem; 
	flex-direction: column-reverse; 
	margin-left: 8%;
}

@media (min-width: 768px) { 
	.contact{
		padding-top: 2.5rem;
		padding-bottom: 2.5rem; 
		margin-top: 2.5rem; 
		flex-direction: row;
	} 
 }
</style>
