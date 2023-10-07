<script>
import feather from 'feather-icons';
import Button from './reusable/Button.vue';
import FormInput from './reusable/FormInput.vue';
import FormTextarea from './reusable/FormTextarea.vue';
export default {
	props: ['showModal', 'modal', 'categories'],
	components: { Button, FormInput, FormTextarea },
	data() {
		return {};
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
	<transition name="fade">
		<div v-show="modal" class="body">
			<!-- Modal body background as backdrop -->
			<div
				v-show="modal"
				@click="showModal()"
				class="overlay"
			></div>
			<!-- Modal content -->
			<main
				class="my-flex-container"
			>
				<transition name="fade-up-down">
					<div
						v-show="modal"
						class="modal-wrapper"
					>
						<div
							class="modal bg-secondary-light dark-bg-primary-dark max-h-screen "
						>
							<div
								class="modal-header"
							>
								<h5
									class="text-primary-dark dark:text-primary-light text-xl"
								>
									What project are you looking for?
								</h5>
								<button
									class="px-4 text-primary-dark dark:text-primary-light"
									@click="showModal()"
								>
									<i data-feather="x"></i>
								</button>
							</div>
							<div class="modal-body p-5 w-full h-full">
								<form class="max-w-xl m-4 text-left">
									<FormInput
										label="Full Name"
										inputIdentifier="name"
										class="mb-2"
									/>
									<FormInput
										label="Email"
										inputIdentifier="email"
										inputType="email"
									/>

									<div class="mt-6 mb-4">
										<label
											class="block mb-2 text-lg text-primary-dark dark:text-primary-light"
											for="project"
											>Project Type</label
										>
										<select
											class="my-custom-class"
											id="project"
											name="project"
											type="text"
											required=""
											aria-label="Project Category"
										>
											<option
												v-for="category in categories"
												:key="category.id"
												:value="category.value"
											>
												{{ category.name }}
											</option>
										</select>
									</div>

									<FormTextarea
										label="Details"
										textareaIdentifier="details"
									/>

									<div class="mt-7 pb-4 sm:pb-1">
										<Button
											title="Send Request"
											class="my-button"
											type="submit"
											aria-label="Submit Request"
										/>
									</div>
								</form>
							</div>
							<div
								class="modal-footer mt-2 sm:mt-0 py-5 px-8 border0-t text-right"
							>
								<Button
									title="Close"
									class="px-4 sm:px-6 py-2 bg-gray-600 text-primary-light hover:bg-ternary-dark dark:bg-gray-200 dark:text-secondary-dark dark:hover:bg-primary-light rounded-md focus:ring-1 focus:ring-indigo-900 duration-500 "
									@click="showModal()"
									aria-label="Close Modal"
								/>
							</div>
						</div>
					</div>
				</transition>
			</main>
		</div>
	</transition>
</template>

<style scoped>
.modal-body {
	max-height: 570px;
}
.bg-gray-800-opacity {
	background-color: #2d374850;
}
@media screen and (max-width: 768px) {
	.modal-body {
		max-height: 400px;
	}
}
.fade-up-down-enter-active {
	transition: all 0.3s ease;
}
.fade-up-down-leave-active {
	transition: all 0.3s ease;
}
.fade-up-down-enter {
	transform: translateY(10%);
	opacity: 0;
}
.fade-up-down-leave-to {
	transform: translateY(10%);
	opacity: 0;
}

.fade-enter-active {
	-webkit-transition: opacity 2s;
	transition: opacity 0.3s;
}
.fade-leave-active {
	transition: opacity 0.3s;
}

.fade-enter,
.fade-leave-to {
	opacity: 0;
}
.body{
	position: fixed; 
top: 0;
right: 0;
bottom: 0;
left: 0; 
z-index: 30; 
}

.overlay {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 20;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}
.my-flex-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
  width: 100%;
}
.modal-wrapper {
  display: flex;
  align-items: center;
  z-index: 30;
}

.modal-header {
  display: flex;
  justify-content: space-between;
  gap: 1rem; 
  padding: 1.25rem; 
  border-bottom: 1px solid white; 
}


.dark .modal-header {
  border-color: red;
}

.text-primary-dark {
  color: #333;
}

.dark .text-primary-light {
  color: #fff; 
}

.text-xl {
  font-size: 1.25rem; 
}

.my-custom-class {
  display: block;
  margin-bottom: 2px;
  font-size: 1.125rem; 
  color: #333; 
  border-color: #ccc;
  border-width: 1.5px;
}

.my-custom-class.dark-mode {
  color: #ccc; 
}

.modal {
  max-width: 28rem; 
  margin-left: 1.25rem; 
  background-color: white;
  box-shadow: 0 0.625rem 1.875rem rgba(0, 0, 0, 0.2); 
  border-radius: 0.375rem; 
  position: relative;
}

@media (min-width: 768px) {
  .modal {
    max-width: 48rem; 
  }
}

.bg-secondary-light {
  background-color: white; 
}
.dark-bg-primary-dark {
  background-color: white; 
}

.max-h-screen {
  max-height: 100vh; 
}

.my-button {
  padding-left: 1rem; 
  padding-right: 1rem; 
  padding-top: 0.5rem; 
  padding-bottom: 0.625rem;
  color: #fff; 
  background-color: #6b46c1; 
  border-radius: 0.375rem; 
  transition-duration: 0.5s; 
}


.my-button:hover {
  background-color: #805ad5; 
}


.my-button:focus {
  outline: none;
  box-shadow: 0 0 0 2px #6b46c1, 0 0 0 4px rgba(107, 70, 193, 0.6);
}


.px-4 {
  padding-left: 1rem;
  padding-right: 1rem;
}

.sm\:px-6 {
  padding-left: 1.5rem;
  padding-right: 1.5rem;
}

.py-2 {
  padding-top: 0.5rem;
  padding-bottom: 0.5rem;
}


.bg-gray-600 {
  background-color: #343a44; 
}

.dark\:bg-gray-200 {
  background-color: #f7fafc; 
}


.text-primary-light {
  color: #FFFFFF; 
}

.dark\:text-secondary-dark {
  color: #2D3748; 
}


.hover\:bg-ternary-dark:hover {
  background-color: #2D3748;
}

.dark\:hover\:bg-primary-light:hover {
  background-color: #FFFFFF; 
}
.rounded-md {
  border-radius: 0.375rem; 
}

.focus\:ring-1:focus {
  box-shadow: 0 0 0 0.125rem rgba(31, 41, 55, 0.25); 
}

.focus\:ring-indigo-900:focus {
  box-shadow: 0 0 0 0.125rem #4f46e5;
}

.duration-500 {
  transition-duration: 0.5s;
}
</style>
