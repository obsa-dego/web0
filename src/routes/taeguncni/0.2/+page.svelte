<script>
	// 버전 0.2 페이지
</script>

<svelte:head>
	<title>taeguncni v0.2 - Rain App</title>
</svelte:head>

<div class="page">
	<div class="header">
		<div class="title">
			<span class="bracket">[</span>
			<span class="title-text">taeguncni v0.2</span>
			<span class="bracket">]</span>
		</div>
	</div>

	<div class="content-section">
		<div class="content-item">
			<span class="content-number">[1]</span>
			<span class="content-text">현장명을 입력할 수 없는 버그가 수정되었습니다</span>
		</div>
	</div>

	<div class="back-section">
		<a href="/taeguncni" class="back-link">
			<span class="back-arrow">&lt;-</span>
			<span class="back-text">back to versions</span>
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
		max-width: 600px;
		display: flex;
		flex-direction: column;
		gap: 0;
	}

	.content-item {
		background: #000;
		border: 1px solid #222;
		padding: 20px 24px;
		display: flex;
		align-items: flex-start;
		gap: 12px;
		font-size: 14px;
		letter-spacing: 0.5px;
		line-height: 1.6;
	}

	.content-number {
		color: #666;
		font-weight: bold;
		min-width: 30px;
		margin-top: 2px;
	}

	.content-text {
		color: #fff;
		flex: 1;
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

		.content-item {
			padding: 16px 20px;
			font-size: 13px;
		}
	}
</style>