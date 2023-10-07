<script>
export default {
	props: {
		select: {
			type: String,
			default: 'projects',
			required: true,
		},
		selectOptions: {
			type: Array,
			default: () => [
				'Web Application',
				'Mobile Application',
				'Software Development',
				'CRM Development',
			],
		},
	},
};
</script>

<template>
	<select
		@change="$emit('filter', $event.target.value)"
		:name="select"
		:id="select"
		class="select"
	>
		<option value class="option">All Projects</option>
		<option
			v-for="option in selectOptions"
			:key="option"
			:value="option"
		>
			{{ option }}
		</option>
	</select>
</template>

<style scoped>
.select{
	padding-top: 0.5rem;
	padding-bottom: 0.5rem; 
	padding-left: 1rem;
	padding-right: 1rem; 
	border-radius: 0.5rem; 
	border-color: #E5E7EB; 
	font-size: 0.875rem;
	line-height: 1.25rem; 
}

.option{
	font-size: 0.875rem;
	line-height: 1.25rem; 
}
</style>
