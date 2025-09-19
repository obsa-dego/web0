<script>
	let versionItems = [
		{ version: '0.3', date: '250919' },
		{ version: '0.2', date: '250918' },
		{ version: '0.1', date: '250918' }
	];

	function handleVersionClick(version) {
		window.location.href = `/taeguncni/${version}`;
	}
</script>

<svelte:head>
	<title>taeguncni - isopng</title>
</svelte:head>

<div class="page">
	<div class="header">
		<div class="title">
			<span class="bracket">[</span>
			<span class="title-text">taeguncni</span>
			<span class="bracket">]</span>
		</div>
	</div>

	<div class="version-section">
		{#each versionItems as item, index}
			<a href="/taeguncni/{item.version}" class="version-item version-link">
				<div class="version-left">
					<span class="version-number">[{index + 1}]</span>
					<span class="version-text">{item.version}</span>
				</div>
				<span class="version-date">{item.date}</span>
			</a>
		{/each}

		<a href="/taeguncni/info" class="version-item version-link info-item">
			<div class="version-left">
				<span class="version-number">[i]</span>
				<span class="version-text">info</span>
			</div>
			<span class="version-date">packages</span>
		</a>
	</div>

	<div class="back-section">
		<a href="/" class="back-link">
			<span class="back-arrow">&lt;-</span>
			<span class="back-text">back</span>
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
		font-size: 28px;
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

	.version-section {
		width: 100%;
		max-width: 300px;
		display: flex;
		flex-direction: column;
		gap: 0;
	}

	.version-item {
		background: #000;
		border: 1px solid #222;
		border-bottom: none;
		padding: 16px 20px;
		cursor: pointer;
		display: flex;
		align-items: center;
		gap: 12px;
		font-size: 14px;
		letter-spacing: 0.5px;
	}

	.version-item:last-child {
		border-bottom: 1px solid #222;
	}

	.version-item:hover {
		background: #111;
		border-color: #444;
	}

	.version-number {
		color: #666;
		font-weight: bold;
		min-width: 30px;
	}

	.version-text {
		color: #fff;
	}

	.version-item:hover .version-text {
		color: #ff0000;
	}

	.version-item:hover .version-number {
		color: #999;
	}

	.version-link {
		text-decoration: none;
		color: inherit;
		display: flex;
		align-items: center;
		justify-content: space-between;
		width: 100%;
	}

	.version-left {
		display: flex;
		align-items: center;
		gap: 12px;
	}

	.version-date {
		color: #555;
		font-size: 11px;
		font-weight: normal;
		letter-spacing: 0.5px;
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
			font-size: 24px;
		}

		.version-item {
			padding: 14px 16px;
			font-size: 13px;
		}

		.back-link {
			padding: 10px 14px;
			font-size: 13px;
		}
	}
</style>