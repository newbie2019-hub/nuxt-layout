<template>
	<nav class="navbar border-bottom">
		<div class="container">
			<a
				class="navbar-brand"
				href="#"
			>
				<img
					src="~/assets/images/logo.svg"
					alt="Bootstrap"
					width="120"
				/>
			</a>
			<div></div>
		</div>
	</nav>
	<nav
		style="--bs-breadcrumb-divider: '>'"
		aria-label="breadcrumb "
		class="border-bottom"
	>
		<div class="container mt-3 d-flex justify-content-between">
			<ol class="breadcrumb">
				<li
					v-for="link in links"
					:key="i"
					class="breadcrumb-item"
				>
					<a
						href="#"
						class="link link-underline link-underline-opacity-0"
						>{{ link }}</a
					>
				</li>
			</ol>
			<div class="d-none d-sm-none d-md-flex">
				<span class="me-2">Sponsor</span>
				<div class="form-check form-switch">
					<input
						class="form-check-input bg-warning"
						type="checkbox"
						role="switch"
						id="flexSwitchCheckDefault"
					/>
				</div>
				<span>Creator</span>
			</div>
			<div class="d-none d-sm-none d-md-block">
				<p>Profile Completeness <span>90%</span></p>
				<div
					class="progress"
					role="progressbar"
					aria-label="Profile Completeness"
					aria-valuenow="50"
					aria-valuemin="0"
					aria-valuemax="100"
				>
					<div
						class="progress-bar bg-warning"
						style="width: 90%"
					></div>
				</div>
			</div>
		</div>
		<div class="container mb-3 d-flex">
			<div class="d-flex d-sm-flex d-md-none d-lg-none justify-content-between" style="width: 100%">
				<div class="d-flex">
					<span class="me-2">Sponsor</span>
					<div class="form-check form-switch">
						<input
							class="form-check-input bg-warning"
							type="checkbox"
							role="switch"
							id="flexSwitchCheckDefault"
						/>
					</div>
					<span>Creator</span>
				</div>
				<div class="">
					<p>Profile Completeness <span>90%</span></p>
					<div
						class="progress"
						role="progressbar"
						aria-label="Profile Completeness"
						aria-valuenow="50"
						aria-valuemin="0"
						aria-valuemax="100"
					>
						<div
							class="progress-bar bg-warning"
							style="width: 90%"
						></div>
					</div>
				</div>
			</div>
		</div>
	</nav>
	<div class="container mt-5">
		<slot />
	</div>
	<hr class="" />
	<div class="d-flex justify-content-between mb-3 px-5">
		<div class="col">
			<p>© 2023 - All rights reserved</p>
		</div>
		<div class="col">
			<div class="d-flex justify-content-between">
				<p>Compensation Calculator</p>
				<p>Affiliates</p>
				<p>Contact Us</p>
				<p>Support</p>
				<p>Our Partners</p>
				<p>Team</p>
			</div>
		</div>
	</div>
</template>
<script setup>
const links = ["Dashboard", "Sponsor Profile", "Verification"];
</script>

<style scoped>
a.link {
	color: #f29820;
}

p {
	margin-bottom: 0;
}

.progress {
	height: 0.3rem;
}
</style>
