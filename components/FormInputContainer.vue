<template>
	<div class="border pt-4 pb-3 px-4 rounded position-relative">
		<div class="text">
			<p class="fs-6 fw-semibold">{{ text }}</p>
		</div>
		<div class="switch">
			<div class="form-check form-switch">
				<input
					class="form-check-input bg-warning"
					type="checkbox"
					role="switch"
					id="flexSwitchCheckDefault"
				/>
			</div>
		</div>
		<slot />
	</div>
</template>
<script setup>
defineProps({
	text: {
		type: String,
    required: true
	},
});
</script>
<style scoped>
.text {
	position: absolute;
	top: -13px;
	left: 15px;
	background-color: white;
	padding: 0 6px;
}

.switch {
	position: absolute;
	top: -13px;
	right: 15px;
	background-color: white;
	padding: 0 0px 0 8px;
}
</style>
