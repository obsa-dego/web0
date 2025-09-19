<script>
	// Page 7 - 404 Error
</script>

<svelte:head>
	<title>404 - Not Found</title>
</svelte:head>

<div class="page">
	<div class="error-container">
		<div class="error-code">404</div>
		<div class="error-message">Not Found</div>
		<div class="error-description">
			The page you are looking for could not be found.
		</div>
	</div>

	<div class="back-section">
		<a href="/knight-view" class="back-link">
			<span class="back-arrow">&lt;-</span>
			<span class="back-text">back to knight view</span>
		</a>
	</div>
</div>

<style>
	.page {
		width: 100%;
		min-height: 100vh;
		background: #000;
		color: #fff;
		font-family: 'Courier New', monospace;
		padding: 60px 20px;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 80px;
	}

	.header {
		text-align: center;
	}

	.title {
		font-size: 24px;
		font-weight: normal;
		letter-spacing: 2px;
	}

	.bracket {
		color: #666;
	}

	.title-text {
		color: #fff;
		margin: 0 8px;
	}

	.error-container {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 20px;
		text-align: center;
	}

	.error-code {
		font-size: 120px;
		font-weight: bold;
		color: #333;
		letter-spacing: 5px;
		line-height: 1;
	}

	.error-message {
		font-size: 24px;
		color: #555;
		letter-spacing: 2px;
		text-transform: uppercase;
	}

	.error-description {
		font-size: 14px;
		color: #666;
		letter-spacing: 0.5px;
		margin-top: 10px;
	}

	.back-section {
		margin-top: auto;
	}

	.back-link {
		display: flex;
		align-items: center;
		gap: 8px;
		color: #666;
		text-decoration: none;
		font-size: 14px;
		letter-spacing: 0.5px;
		border: 1px solid #333;
		padding: 12px 16px;
		background: #000;
	}

	.back-link:hover {
		background: #111;
		border-color: #555;
		color: #fff;
	}

	.back-arrow {
		color: #666;
	}

	.back-text {
		color: inherit;
	}

	@media (max-width: 768px) {
		.page {
			padding: 40px 15px;
			gap: 60px;
		}

		.error-code {
			font-size: 80px;
		}

		.error-message {
			font-size: 20px;
		}

		.error-description {
			font-size: 13px;
		}
	}
</style>