<script>
	let email = '';
	let emailValid = true;

	// Function to check if the email is valid
	function checkEmail() {
		if (email.includes('@') && email.includes('.')) {
			emailValid = true;
			// Redirect with email in URL
			window.location.href = `/success?email=${encodeURIComponent(email)}`;
		} else {
			emailValid = false;
		}
		return emailValid;
	}

	// Reset the email validity when the user starts typing
	function handleInput() {
		if (!emailValid) {
			emailValid = true;
		}
	}
</script>

<div class="h-screen w-screen bg-hsl-[235_18%_26%] flex justify-center items-center">
	<div
		class="bg-white text-black rounded-3xl shadow-lg w-3/5 h-3/4 flex flex-col-reverse lg:flex-row justify-between items-center p-6 overflow-hidden"
	>
		<div class="max-w-1/2 pl-10">
			<h1 class="text-5xl font-bold mb-6">Stay updated!</h1>
			<p class="mb-0">Join 60,000+ product managers receiving monthly updates on:</p>
			<div class="flex items-center mb-1">
				<img src="assets/images/icon-list.svg" alt="Check" class="w-5 h-5 mr-3" />
				<p>Product discovery and building what matters</p>
			</div>
			<div class="flex items-center mb-1">
				<img src="assets/images/icon-list.svg" alt="Check" class="w-5 h-5 mr-3" />
				<p class="mb-1">Measuring to ensure updates are a success</p>
			</div>
			<div class="flex items-center mb-4">
				<img src="assets/images/icon-list.svg" alt="Check" class="w-5 h-5 mr-3" />
				<p class="mb-1">And much more!</p>
			</div>

			<div class="flex items-center justify-between w-4/5 mb-2">
				<p class="text-xs font-bold">Email address</p>
				{#if !emailValid}
					<p class="text-red-500 text-xs font-bold">Valid email required</p>
				{/if}
			</div>

			<input
				bind:value={email}
				type="text"
				placeholder="Email@company.com"
				class="bg-white border rounded-md w-4/5 px-4 py-2 focus:outline-none focus:ring-0 mb-2
		  {emailValid ? 'border-gray-300' : 'border-red-500 text-red-500 bg-red-50'}"
				on:input={handleInput}
			/>

			<button
				class="btn btn-active btn-neutral bg-gradient-to-r hover:from-orange-500 hover:to-pink-500 hover:outline-0 text-white py-2 px-4 rounded-md transition-all duration-300"
				on:click={checkEmail}
			>
				Subscribe to monthly newsletter
			</button>
		</div>

		<div class="flex items-center justify-center h-full p-0 flex-shrink-0">
			<img
				class="w-auto h-full object-contain"
				src="assets/images/illustration-sign-up-desktop.svg"
				alt="Illustration"
			/>
		</div>
	</div>
</div>
