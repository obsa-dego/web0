<script>
	let changeItems = [
		'분석 결과 화면의 레이아웃이 변경되었습니다',
		'분석 결과에서 그림을 그릴 수 없는 오류가 수정되었습니다',
		'AI가 화재 청소에 대해 분석하지 않는 오류가 수정되었습니다',
		'분석 결과 화면에서 작업 체크리스트 금액 입력란 콤마 미표기 오류가 수정되었습니다',
		'그 외 세부 편의성 및 오류 개선'
	];

	let showPasswordInput = false;
	let password = '';
	let passwordError = false;

	function requestDownload() {
		console.log('Download button clicked');
		showPasswordInput = true;
		passwordError = false;
		console.log('showPasswordInput set to:', showPasswordInput);
	}

	function handlePasswordSubmit() {
		if (password === '1234') {
			// Start download
			const link = document.createElement('a');
			link.href = '/app-release.apk';
			link.download = 'taeguncni-v0.3.apk';
			document.body.appendChild(link);
			link.click();
			document.body.removeChild(link);

			// Reset state
			showPasswordInput = false;
			password = '';
		} else {
			passwordError = true;
		}
	}

	function cancelDownload() {
		showPasswordInput = false;
		password = '';
		passwordError = false;
	}
</script>

<svelte:head>
	<title>taeguncni v0.3 - Rain App</title>
</svelte:head>

<div class="page">
	<div class="header">
		<div class="title">
			<span class="bracket">[</span>
			<span class="title-text">taeguncni v0.3</span>
			<span class="bracket">]</span>
		</div>
	</div>

	<div class="content-section">
		{#each changeItems as item, index}
			<div class="content-item">
				<span class="content-number">[{index + 1}]</span>
				<span class="content-text">{item}</span>
			</div>
		{/each}
	</div>

	<div class="download-section">
		{#if !showPasswordInput}
			<div class="download-item">
				<span class="download-number">[APK]</span>
				<button on:click={requestDownload} class="download-button" type="button">
					<span class="download-text">앱 다운로드 (APK)</span>
				</button>
			</div>
		{:else}
			<div class="password-form">
				<div class="password-header">
					<span class="password-title">다운로드 비밀번호 입력</span>
				</div>
				<div class="password-input-container">
					<input
						type="password"
						bind:value={password}
						placeholder="비밀번호 입력"
						class="password-input"
						on:keydown={(e) => e.key === 'Enter' && handlePasswordSubmit()}
					/>
					<div class="password-buttons">
						<button on:click={handlePasswordSubmit} class="password-submit">확인</button>
						<button on:click={cancelDownload} class="password-cancel">취소</button>
					</div>
				</div>
				{#if passwordError}
					<div class="password-error">잘못된 비밀번호입니다</div>
				{/if}
			</div>
		{/if}
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
		align-items: flex-start;
		gap: 12px;
		font-size: 13px;
		letter-spacing: 0.5px;
		line-height: 1.5;
	}

	.content-item:last-child {
		border-bottom: 1px solid #222;
	}

	.content-number {
		color: #666;
		font-weight: bold;
		min-width: 30px;
		margin-top: 1px;
	}

	.content-text {
		color: #fff;
		flex: 1;
	}

	.download-section {
		width: 100%;
		max-width: 700px;
		margin-top: 20px;
	}

	.download-item {
		background: #000;
		border: 1px solid #333;
		padding: 18px 24px;
		display: flex;
		align-items: center;
		gap: 12px;
		font-size: 13px;
		letter-spacing: 0.5px;
	}

	.download-number {
		color: #666;
		font-weight: bold;
		min-width: 50px;
	}

	.download-button {
		background: transparent;
		border: none;
		color: #fff;
		font-family: 'Courier New', monospace;
		font-size: 13px;
		letter-spacing: 0.5px;
		cursor: pointer;
		transition: color 0.3s ease;
		padding: 0;
	}

	.download-button:hover {
		color: #ff0000;
	}

	.download-text {
		color: inherit;
	}

	.password-form {
		background: #000;
		border: 1px solid #333;
		padding: 20px;
		width: 100%;
	}

	.password-header {
		margin-bottom: 15px;
		text-align: center;
	}

	.password-title {
		color: #fff;
		font-size: 13px;
		font-weight: bold;
		letter-spacing: 0.5px;
	}

	.password-input-container {
		display: flex;
		flex-direction: column;
		gap: 12px;
	}

	.password-input {
		background: #111;
		border: 1px solid #333;
		color: #fff;
		font-family: 'Courier New', monospace;
		font-size: 13px;
		padding: 10px 12px;
		letter-spacing: 0.5px;
	}

	.password-input:focus {
		outline: none;
		border-color: #666;
	}

	.password-input::placeholder {
		color: #666;
	}

	.password-buttons {
		display: flex;
		gap: 10px;
		justify-content: center;
	}

	.password-submit,
	.password-cancel {
		background: #000;
		border: 1px solid #333;
		color: #fff;
		font-family: 'Courier New', monospace;
		font-size: 12px;
		padding: 8px 16px;
		cursor: pointer;
		letter-spacing: 0.5px;
		transition: all 0.3s ease;
	}

	.password-submit:hover {
		background: #111;
		border-color: #555;
		color: #ff0000;
	}

	.password-cancel:hover {
		background: #111;
		border-color: #555;
		color: #888;
	}

	.password-error {
		color: #ff0000;
		font-size: 12px;
		text-align: center;
		margin-top: 10px;
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
			font-size: 20px;
		}

		.content-section {
			max-width: 100%;
		}

		.content-item {
			padding: 16px 20px;
			font-size: 12px;
		}

		.download-section {
			max-width: 100%;
		}

		.download-item {
			padding: 16px 20px;
			font-size: 12px;
		}

		.password-form {
			padding: 16px;
		}

		.password-input {
			font-size: 12px;
			padding: 8px 10px;
		}

		.password-submit,
		.password-cancel {
			font-size: 11px;
			padding: 6px 12px;
		}
	}
</style>