<script>
export default {
	props: {
		label: {
			type: String,
			default: '',
		},
		textareaIdentifier: {
			type: String,
			default: '',
		},
		val: {
			type: [String, Number],
			default: '',
		},
	},
};
</script>

<template>
	<div>
		<label
			class="label"
			:for="textareaIdentifier"
			>{{ label }}</label
		>
		<textarea
			class="input"
			:id="textareaIdentifier"
			:name="textareaIdentifier"
			:aria-label="textareaIdentifier"
			:placeholder="label"
			v-bind="$attrs"
			@input="$emit('update:val', $event.target.value)"
			cols="14"
			rows="6"
		></textarea>
	</div>
</template>

<style scoped>
.label{
	display: block; 
	margin-bottom: 0.5rem; 
	font-size: 1.125rem;
	line-height: 1.75rem; 
}
.input{
	padding-top: 0.75rem;
	padding-bottom: 0.75rem; 
	padding-left: 1.25rem;
	padding-right: 1.25rem; 
	border-radius: 0.375rem; 
	border-width: 1px; 
	border-color: #D1D5DB; 
	border-opacity: 0.5; 
	width: 100%; 
	box-shadow: 0 1px 2px 0 rgba(0, 0, 0, 0.05); 
}
</style>
