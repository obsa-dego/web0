<script>
	// Page 1 - Simple greeting
</script>

<svelte:head>
	<title>Knight View - Page 1</title>
</svelte:head>

<div class="page">
	<div class="header">
		<div class="title">
			<span class="bracket">[</span>
			<span class="title-text">knight view - page 1</span>
			<span class="bracket">]</span>
		</div>
	</div>

	<div class="content-section">
		<div class="content-item">
			<span class="content-text">hi</span>
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

	.content-section {
		width: 100%;
		max-width: 700px;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 0;
	}

	.content-item {
		background: #000;
		border: 1px solid #222;
		padding: 40px 60px;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 24px;
		letter-spacing: 1px;
		text-align: center;
	}

	.content-text {
		color: #fff;
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

		.title {
			font-size: 20px;
		}

		.content-section {
			max-width: 100%;
		}

		.content-item {
			padding: 30px 40px;
			font-size: 20px;
		}
	}
</style>