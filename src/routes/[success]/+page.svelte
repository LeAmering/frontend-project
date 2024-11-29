<script>
	import { onMount } from 'svelte';

	let email = '';

	onMount(() => {
		const urlParams = new URLSearchParams(window.location.search);
		email = urlParams.get('email');
	});
</script>

<div class="h-screen w-screen bg-hsl-[235_18%_26%] flex justify-center items-center">
	<div
		class="bg-white text-black rounded-3xl shadow-lg lg:w-3/5 lg:h-3/4 flex flex-col-reverse lg:flex-row justify-between items-center p-6 overflow-hidden"
	>
		<div class="max-w-1/2 pl-10">
			<div>
				<img src="assets/images/icon-success.svg" alt="check" class="mb-7 mt-2" />
			</div>
			<h1 class="text-5xl font-bold mb-6">Thanks for subscribing!</h1>
			<p class="mb-4">
				A confirmation email has been sent to {email}. Please open it and klick the button inside to
				confirm your subscription.
			</p>

			<button
				class="btn btn-active btn-neutral bg-gradient-to-r hover:from-orange-500 hover:to-pink-500 hover:outline-0 text-white py-2 px-4 rounded-md transition-all duration-300"
				onclick={(window.location.href = '/')}>Dismiss message</button
			>
		</div>
	</div>
</div>
