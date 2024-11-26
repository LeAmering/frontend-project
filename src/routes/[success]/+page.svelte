<script>
	let { email } = $props();
</script>

<div class="h-screen w-screen bg-hsl-[235_18%_26%] flex justify-center items-center">
	<div
		class="bg-white text-black rounded-3xl shadow-lg w-3/5 h-3/4 flex justify-between items-start p-6 overflow-hidden"
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

			<button class="btn btn-active btn-neutral" onclick={(window.location.href = '/')}
				>Dismiss message</button
			>
		</div>
	</div>
</div>
