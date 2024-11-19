<script>
</script>

<div class="white-box">
	<div class="text-content">
		<h1>Stay updated!</h1>
		<p>Join 60.000+ product managers receiving monthly updates on:</p>
		<p>Product discovery and building what matters</p>
		<p>Measuring to ensure updates are a success</p>
		<p>And much more!</p>

		<input
			type="text"
			placeholder="Email@company.com"
			class="input input-bordered w-full max-w-xs"
			style="background-color:white"
		/>
	</div>

	<div class="image-container">
		<img
			class="signup-image"
			src="assets/images/illustration-sign-up-desktop.svg"
			alt="Illustration"
		/>
	</div>
</div>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		background-color: hsl(235, 18%, 26%);
		font-family: Arial, sans-serif;
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
		color: white;
	}

	.white-box {
		background-color: white;
		color: black;
		width: 75%;
		height: 75%;
		border-radius: 30px;
		box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 20px;
		text-align: left;
		overflow: hidden;
	}

	.text-content {
		max-width: 50%;
	}

	h1 {
		font-size: 25px;
	}

	.image-container {
		display: flex;
		align-items: center;
		justify-content: center;
		padding: 20px;
		flex-shrink: 0;
		height: 100%;
	}

	.signup-image {
		max-width: 100%;
		height: auto;
		object-fit: contain;
		padding-top: 20px;
		padding-bottom: 20px;
	}

	.input {
		width: 80%;
	}
</style>
