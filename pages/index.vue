<template>
	<NuxtLayout>
		<div class="row justify-content-between">
			<div class="col-12 col-md-5 col-lg-4 mb-4">
				<ProfileCardContainer />
			</div>
			<div class="col-12 col-md-7 col-lg-8">
				<FormInputContainer text="Verify phone number">
					<div class="row gx-2">
						<div class="col">
							<div class="form-floating mb-3">
								<input
									type="email"
									class="form-control"
									id="floatingInput"
									placeholder=" "
								/>
								<label for="floatingInput">Select country code</label>
							</div>
						</div>
						<div class="col">
							<div class="form-floating mb-3">
								<input
									type="text"
									class="form-control"
									id="floatingPhoneNumber"
									placeholder=" "
								/>
								<label for="floatingPhoneNumber">Phone Number</label>
							</div>
						</div>
					</div>
				</FormInputContainer>
				<FormInputContainer
					text="Verify Email"
					class="mt-4"
				>
					<div class="col-sm-10">
						<input
							type="text"
							readonly
							class="form-control-plaintext"
							id="staticEmail"
							value="email@example.com"
						/>
					</div>
				</FormInputContainer>
				<FormInputContainer
					text="Verify Identity"
					class="mt-4"
				>
					<p>Choose an ID type to add</p>
					<div class="row gx-2 mt-2">
						<div class="col">
							<select
								class="form-select"
								aria-label="Issuing country/region"
							>
								<option selected>Issuing country/region</option>
							</select>
						</div>
						<div class="col">
							<select
								class="form-select"
								aria-label="Choose identification"
							>
								<option selected>Choose identification</option>
							</select>
						</div>
					</div>
					<hr class="mt-4" />
					<p>Upload images of your ID</p>
					<div class="row gx-2 mt-2">
						<div class="col">
							<div class="card py-4 px-5 d-flex justify-content-center text-center">
								<img
									src="~/assets/images/front-icon.png"
									alt="Upload Back Image"
									width="40"
									class="img-center"
								/>
								<p class="fs-5 mt-2">Upload front</p>
								<p class="text-secondary">JPEG or PNG only</p>
								<input
									type="file"
									id="uploadFrontPhoto"
									style="display: none"
								/>
								<label
									for="uploadFrontPhoto"
									class="btn btn-warning-2 rounded-pill text-white mt-2"
								>
									Select Files
								</label>
							</div>
						</div>
						<div class="col">
							<div class="card py-4 px-5 d-flex justify-content-center text-center">
								<img
									src="~/assets/images/back-icon.png"
									alt="Upload Back Image"
									width="40"
									class="img-center"
								/>
								<p class="fs-5 mt-2">Upload back</p>
								<p class="text-secondary">JPEG or PNG only</p>
								<input
									type="fileBack"
									id="uploadBackPhoto"
									style="display: none"
								/>
								<label
									for="uploadBackPhoto"
									class="btn btn-warning-2 rounded-pill text-white mt-2"
								>
									Select Files
								</label>
							</div>
						</div>
					</div>
					<hr class="mt-4" />
					<p>Take a photo of yourself with your ID</p>
					<div
						class="card py-4 px-5 d-flex justify-content-center text-center mb-3 mt-2"
					>
						<img
							src="~/assets/images/upload-icon.png"
							alt="Upload Selfie"
							width="50"
							class="img-center"
						/>
						<p class="fs-5 mt-2">Upload back</p>
						<p class="text-secondary">JPEG or PNG only</p>
						<input
							type="file"
							id="uploadPhoto"
							style="display: none"
						/>
						<label
							for="uploadPhoto"
							class="btn btn-warning-2 rounded-pill text-white mt-2"
						>
							Select Files
						</label>
					</div>
				</FormInputContainer>
			</div>
			<hr class="mt-5 mb-3" />
			<div class="d-flex justify-content-end mb-4">
				<button
					type="button"
					class="btn btn-warning-2 rounded-pill text-white mt-2"
				>
					Save & Synchronize
				</button>
			</div>
		</div>
	</NuxtLayout>
</template>
<script setup></script>
<style>
.btn-warning-2 {
	background-color: #f29820;
}

.btn-warning-2:hover {
	background-color: #e28b19;
}

.btn-warning-2:active {
	background-color: #f29820 !important;
}

.img-center {
	display: block;
	margin-left: auto;
	margin-right: auto;
}
</style>
