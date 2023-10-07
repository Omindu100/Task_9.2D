<script>
import Button from '../reusable/Button.vue';
import FormInput from '../reusable/FormInput.vue';
import FormTextarea from '../reusable/FormTextarea.vue';
export default { components: { Button, FormInput, FormTextarea } };
</script>

<template>
	<div class="w-full md:w-1/2">
		<div
			class="form"
		>
			<p
				class="header"
			>
				Contact Form
			</p>
			<form action="#" class="font">
				<FormInput label="Full Name" inputIdentifier="name" />
				<FormInput
					label="Email"
					inputIdentifier="email"
					inputType="email"
					class="font"
				/>
				<FormInput label="Subject" inputIdentifier="subject" class="font"/>
				<FormTextarea label="Message" textareaIdentifier="message" class="font"/>

				<div>
					<Button
						title="Send Message"
						class="submit"
						type="submit"
						aria-label="Send Message"
					/>
				</div>
			</form>
		</div>
	</div>
</template>

<style scoped>
.form{
	padding: 2rem; 
	border-radius: 0.75rem; 
	max-width: 36rem; 
	line-height: 2; 
	text-align: left; 
	box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04); 
}
.header{
	margin-bottom: 2rem; 
	font-size: 1.5rem;
	line-height: 2rem; 
}
.submit{
	padding-top: 0.625rem;
	padding-bottom: 0.625rem; 
	padding-left: 1rem;
	padding-right: 1rem; 
	border-radius: 0.5rem; 
	letter-spacing: 0.05em; 
	color: #ffffff; 
	background-color: #6366F1; 
	transition-duration: 500ms; 
}
.submit:hover {
 background-color: #4F46E5; 
 }
 .font{
	font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
	color: #262523;
	margin-top: 5%;
 }
</style>
