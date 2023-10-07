<script>
export default {
	props: {
		label: {
			type: String,
			default: '',
		},
		inputIdentifier: {
			type: String,
			default: '',
		},
		val: {
			type: [String, Number],
			default: '',
		},
		inputType: {
			type: String,
			default: 'text',
		},
	},
};
</script>

<template>
	<div>
		<label
			class="label"
			:for="label"
			>{{ label }}</label
		>
		<input
			class="input"
			:id="inputIdentifier"
			:name="inputIdentifier"
			:placeholder="label"
			:aria-label="inputIdentifier"
			:value="val"
			:type="inputType"
			v-bind="$attrs"
			@input="$emit('update:val', $event.target.value)"
			required
		/>
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
