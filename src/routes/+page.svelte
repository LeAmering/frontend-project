<script>
	function checkEmail() {
		const email = document.querySelector('input').value;
		console.log(email);

		if (email.includes('@') && email.includes('.')) {
			window.location.href = '/success';
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
			<h1 class="text-5xl font-bold mb-6">Stay updated!</h1>
			<p class="mb-0">Join 60.000+ product managers receiving monthly</p>

			<p class="mb-4">updates on:</p>
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
			<p class="text-xs font-bold mt-3">Email address</p>
			<input
				type="text"
				placeholder="Email@company.com"
				class="bg-white border border-gray-300 rounded-md w-4/5 px-4 py-2 focus:outline-none focus:ring focus:ring-blue-500 mb-2"
			/>
			<button class="btn btn-active btn-neutral" onclick={checkEmail}
				>Subscribe to monthly newsletter</button
			>
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
