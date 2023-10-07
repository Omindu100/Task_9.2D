<script>
export default {
	data: () => {
		return {
			copyrightDate: new Date().getFullYear(),
			projectName: 'Portfolio Website',
			author: 'Omindu Weragodage',
		};
	},
};
</script>

<template>
	<div class="copy_right">
		<div
			class="footer_copyright"
		>
			&copy; {{ copyrightDate }}.
			{{ projectName }}
			. Developed by
			{{ author }}
		</div>
	</div>
</template>

<style scoped>
.copy_right{
	display: flex; 
	justify-content: center; 
	align-items: center; 
	text-align: center; 
}
.footer_copyright{
	display: flex; 
	justify-content: center; 
	align-items: center; 
	text-align: center; 
}
</style>
