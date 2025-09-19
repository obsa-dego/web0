<script>
	let menuItems = [
		'taeguncni',
		'git0720',
		'git0821',
		'sveltekit route',
		'flutter pub collection',
		'knight view'
	];

	function handleItemClick(item) {
		console.log('Clicked:', item);
		if (item === 'taeguncni') {
			console.log('Opening taeguncni page');
			window.open('/taeguncni', '_blank');
		}
		if (item === 'knight view') {
			window.location.href = '/knight-view';
		}
	}
</script>

<svelte:head>
	<title>Rain App</title>
</svelte:head>

<div class="page">
	<!-- 이미지 영역 -->
	<div class="image-section">
		<img src="/chagall.jpeg" alt="샤갈" class="main-image" />
	</div>

	<!-- 메뉴 영역 -->
	<div class="menu-section">
		{#each menuItems as item, index}
			{#if item === 'taeguncni'}
				<a href="/taeguncni" class="menu-item menu-link">
					<span class="menu-number">[{index + 1}]</span>
					<span class="menu-text">{item}</span>
				</a>
			{:else if item === 'knight view'}
				<a href="/knight-view" class="menu-item menu-link">
					<span class="menu-number">[{index + 1}]</span>
					<span class="menu-text">{item}</span>
				</a>
			{:else}
				<div class="menu-item" on:click={() => handleItemClick(item)}>
					<span class="menu-number">[{index + 1}]</span>
					<span class="menu-text">{item}</span>
				</div>
			{/if}
		{/each}
	</div>

	<!-- 개발자 정보 -->
	<div class="footer-section">
		<div class="footer-item">
			<span class="footer-label">developed</span>
			<span class="footer-separator">-</span>
			<span class="footer-value">황희성</span>
		</div>
		<div class="footer-item">
			<span class="footer-label">Tech Stack</span>
			<span class="footer-separator">-</span>
			<span class="footer-value">JS , TS , sveltekit</span>
		</div>
	</div>
</div>

<style>
	.page {
		width: 100%;
		min-height: 100vh;
		background: #000;
		color: #fff;
		font-family: 'Courier New', monospace;
		padding: 40px 20px 120px 20px;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 60px;
	}

	.image-section {
		text-align: center;
	}

	.main-image {
		max-width: 400px;
		max-height: 300px;
		width: auto;
		height: auto;
		border: 2px solid #333;
		filter: grayscale(20%);
	}

	.menu-section {
		width: 100%;
		max-width: 500px;
		display: flex;
		flex-direction: column;
		gap: 0;
	}

	.menu-item {
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

	.menu-item:last-child {
		border-bottom: 1px solid #222;
	}

	.menu-item:hover {
		background: #111;
		border-color: #444;
	}

	.menu-number {
		color: #666;
		font-weight: bold;
		min-width: 30px;
	}

	.menu-text {
		color: #fff;
	}

	.menu-item:hover .menu-text {
		color: #ff0000;
	}

	.menu-item:hover .menu-number {
		color: #999;
	}

	.menu-item.disabled {
		cursor: not-allowed;
		opacity: 0.4;
	}

	.menu-item.disabled:hover {
		background: #000;
		border-color: #222;
	}

	.menu-item.disabled:hover .menu-text {
		color: #fff;
	}

	.menu-item.disabled:hover .menu-number {
		color: #666;
	}

	.menu-link {
		text-decoration: none;
		color: inherit;
		display: flex;
		align-items: center;
		gap: 12px;
	}

	.footer-section {
		position: fixed;
		bottom: 20px;
		left: 50%;
		transform: translateX(-50%);
		width: 100%;
		max-width: 500px;
		display: flex;
		flex-direction: column;
		gap: 8px;
	}

	.footer-item {
		display: flex;
		align-items: center;
		gap: 8px;
		font-size: 12px;
		font-weight: bold;
		letter-spacing: 0.5px;
		justify-content: center;
	}

	.footer-label {
		color: #666;
		font-weight: bold;
	}

	.footer-separator {
		color: #444;
		font-weight: bold;
	}

	.footer-value {
		color: #888;
		font-weight: bold;
	}

	@media (max-width: 768px) {
		.page {
			padding: 20px 15px 30px 15px;
			gap: 40px;
		}

		.main-image {
			max-width: 300px;
			max-height: 200px;
		}

		.menu-item {
			padding: 14px 16px;
			font-size: 13px;
		}

		.footer-section {
			bottom: 15px;
		}

		.footer-item {
			font-size: 11px;
		}
	}
</style>