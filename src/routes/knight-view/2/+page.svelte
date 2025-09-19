<script>
	// Page 2 - YouTube video
	const videoId = 'PrFdQ7UNBR0';
	const embedUrl = `https://www.youtube.com/embed/${videoId}`;
</script>

<svelte:head>
	<title>Knight View - Page 2</title>
</svelte:head>

<div class="page">
	<div class="header">
		<div class="title">
			<span class="bracket">[</span>
			<span class="title-text">knight view - page 2</span>
			<span class="bracket">]</span>
		</div>
	</div>

	<div class="content-section">
		<div class="video-container">
			<iframe
				src={embedUrl}
				title="YouTube video player"
				frameborder="0"
				allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
				allowfullscreen
				class="video-iframe"
			></iframe>
		</div>

		<div class="lyrics-section">
			<div class="lyrics-text">
				I'll be honest, I'll be honest<br>
				We all liars<br><br>
				Guess who's goin' to jail tonight?<br>
				God gon' post my bail tonight
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

	.video-container {
		width: 100%;
		max-width: 800px;
		background: #000;
		border: 1px solid #222;
		padding: 20px;
		position: relative;
		aspect-ratio: 16 / 9;
	}

	.video-iframe {
		position: absolute;
		top: 20px;
		left: 20px;
		width: calc(100% - 40px);
		height: calc(100% - 40px);
		border: none;
		background: #111;
	}

	.lyrics-section {
		width: 100%;
		max-width: 800px;
		background: #000;
		padding: 30px;
		text-align: left;
	}

	.lyrics-text {
		color: #fff;
		font-size: 14px;
		letter-spacing: 0.5px;
		line-height: 1.8;
		font-weight: normal;
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

		.video-container {
			max-width: 100%;
			padding: 15px;
		}

		.video-iframe {
			top: 15px;
			left: 15px;
			width: calc(100% - 30px);
			height: calc(100% - 30px);
		}

		.lyrics-section {
			max-width: 100%;
			padding: 20px;
		}

		.lyrics-text {
			font-size: 13px;
		}
	}
</style>