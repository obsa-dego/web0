<script>
	let pageItems = [
		{ name: 'Page 1', disabled: true },
		{ name: 'Page 2', disabled: false },
		{ name: 'Page 3', disabled: false },
		{ name: 'Page 4', disabled: false },
		{ name: 'Page 5', disabled: false },
		{ name: 'Page 6', disabled: true },
		{ name: 'Page 7', disabled: false },
		{ name: 'Page 8', disabled: false }
	];
</script>

<svelte:head>
	<title>Knight View - Rain App</title>
</svelte:head>

<div class="page">
	<div class="header">
		<div class="title">
			<span class="bracket">[</span>
			<span class="title-text">knight view</span>
			<span class="bracket">]</span>
		</div>
	</div>

	<div class="content-section">
		{#each pageItems as item, index}
			<div class="content-item {item.disabled ? 'disabled' : ''}">
				<span class="content-number">[{index + 1}]</span>
				{#if !item.disabled}
					<a href="/knight-view/{index + 1}" class="content-link">
						<span class="content-text">{item.name}</span>
					</a>
				{:else}
					<span class="content-link disabled-link">
						<span class="content-text">{item.name}</span>
					</span>
				{/if}
			</div>
		{/each}
	</div>

	<div class="back-section">
		<a href="/" class="back-link">
			<span class="back-arrow">&lt;-</span>
			<span class="back-text">back to home</span>
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
		gap: 0;
	}

	.content-item {
		background: #000;
		border: 1px solid #222;
		border-bottom: none;
		padding: 18px 24px;
		display: flex;
		align-items: center;
		gap: 12px;
		font-size: 13px;
		letter-spacing: 0.5px;
	}

	.content-item:last-child {
		border-bottom: 1px solid #222;
	}

	.content-item:hover {
		background: #111;
		border-color: #444;
	}

	.content-number {
		color: #666;
		font-weight: bold;
		min-width: 30px;
	}

	.content-link {
		text-decoration: none;
		color: #fff;
		flex: 1;
	}

	.content-text {
		color: inherit;
	}

	.content-item:hover .content-text {
		color: #ff0000;
	}

	.content-item:hover .content-number {
		color: #999;
	}

	.content-item.disabled {
		opacity: 0.3;
		cursor: not-allowed;
	}

	.content-item.disabled:hover {
		background: #000;
		border-color: #222;
	}

	.content-item.disabled .content-text {
		color: #666;
	}

	.content-item.disabled:hover .content-text {
		color: #666;
	}

	.disabled-link {
		cursor: not-allowed;
		flex: 1;
		display: block;
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
			padding: 16px 20px;
			font-size: 12px;
		}
	}
</style>