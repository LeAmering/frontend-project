<script>
	function checkEmail() {
		const email = document.querySelector('input').value;
		console.log(email);

		if (email.includes('@') && email.includes('.')) {
			// go to the success page
		} else {
			//make button red and write invalid
		}
	}
</script>

<div class="h-screen w-screen bg-hsl-[235_18%_26%] flex justify-center items-center">
	<div
		class="bg-white text-black rounded-3xl shadow-lg w-3/5 h-3/4 flex justify-between items-center p-6 overflow-hidden"
	>
		<div class="max-w-1/2 pl-10">
			<h1 class="text-xl font-bold mb-4">Stay updated!</h1>
			<p class="mb-2">Join 60.000+ product managers receiving monthly</p>
			<p class="mb-2">updates on:</p>
			<p class="mb-1">Product discovery and building what matters</p>
			<p class="mb-1">Measuring to ensure updates are a success</p>
			<p class="mb-4">And much more!</p>

			<input
				type="text"
				placeholder="Email@company.com"
				class="bg-white border border-gray-300 rounded-md w-4/5 px-4 py-2 focus:outline-none focus:ring focus:ring-blue-500"
			/>
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

<button class="btn btn-active btn-neutral">Subscribe to monthly newsletter</button>
