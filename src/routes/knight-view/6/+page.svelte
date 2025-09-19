<script>
	// Page 6 - Text only
</script>

<svelte:head>
	<title>Knight View - Page 6</title>
</svelte:head>

<div class="page">
	<div class="header">
		<div class="title">
			<span class="bracket">[</span>
			<span class="title-text">knight view - page 6</span>
			<span class="bracket">]</span>
		</div>
	</div>

	<div class="content-section">
		<div class="text-container">
			<div class="text-content">
				그는 천장에서 떨어지는 물방울을 받아 생명을 이어왔지만, 굶주림은 더 깊어졌다.<br><br>

				가족과 친구의 시신을 먹을 수는 없었다.<br><br>

				그래서 그는 어둠 속에 누워 죽음을 기다렸다.<br><br>

				무엇이 자신을 데려갈지 생각했다.<br>
				질식일까? 가스 누출일까? 굶주림? 탈수? 저체온?<br>
				어쩌면 그저 살아가는 일을 멈춰버릴지도 모른다.<br><br>

				머지않아 그는 답을 알았다.<br><br>

				저 먼 심부에서 무거운 굉음이 울렸다.<br>
				한 번 더.<br>
				또 한 번.<br><br>

				이어지는 충격음은 휘어지는 강철의 비명과 무너져 떨어지는 바위 소리와 뒤섞였다.<br><br>

				동굴이 붕괴하고 있었다.<br><br>

				그는 달아나거나 탈출하려 하지 않았다.<br>
				그저 차갑고 축축한 바닥에 누워,<br>
				돌이 자신의 머리를 먼저 산산이 부수어 주기를 바랐다.
			</div>
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
		max-width: 900px;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 40px;
	}

	.text-container {
		width: 100%;
		max-width: 800px;
		background: #000;
		padding: 40px;
	}

	.text-content {
		color: #fff;
		font-size: 14px;
		letter-spacing: 0.5px;
		line-height: 1.8;
		font-weight: normal;
		text-align: left;
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

		.text-container {
			max-width: 100%;
			padding: 25px;
		}

		.text-content {
			font-size: 13px;
		}
	}
</style>