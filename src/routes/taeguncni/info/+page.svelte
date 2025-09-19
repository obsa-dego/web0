<script>
	let packages = [
		{
			name: 'Flutter',
			description: 'Google\'s UI toolkit for building natively compiled applications',
			link: 'https://flutter.dev'
		},
		{
			name: 'User Model Reference',
			description: 'User model object structure reference - MVVM pattern example',
			link: 'https://github.com/Dev-Adnani/flutter-mvvm-template/blob/main/lib/models/userModel/user.model.dart'
		},
		{
			name: 'MVC Architecture',
			description: 'Model-View-Controller pattern for Flutter apps (pub.dev)',
			link: 'https://pub.dev/packages/mvc_pattern'
		},
		{
			name: 'MVC Controller Reference',
			description: 'MVC Controller implementation example',
			link: 'https://github.com/Gubiar/flutter_mvc/blob/main/lib/controller/UsuarioController.dart'
		},
		{
			name: 'GetX',
			description: 'State management, dependency injection and route management',
			link: 'https://pub.dev/packages/get'
		},
		{
			name: 'Assistant API',
			description: 'OpenAI Assistant API integration',
			link: 'https://pub.dev/packages/dart_openai'
		},
		{
			name: 'Google ML Kit',
			description: 'Google Lens API and ML features',
			link: 'https://pub.dev/packages/google_mlkit_text_recognition'
		},
		{
			name: 'Supabase Flutter',
			description: 'Supabase backend integration',
			link: 'https://pub.dev/packages/supabase_flutter'
		},
		{
			name: 'Supabase Functions',
			description: 'Edge Functions (included in supabase_flutter)',
			link: 'https://pub.dev/packages/supabase_flutter'
		},
		{
			name: 'Intl',
			description: 'Internationalization and localization',
			link: 'https://pub.dev/packages/intl'
		},
		{
			name: 'Image Picker',
			description: 'Select images from gallery or camera',
			link: 'https://pub.dev/packages/image_picker'
		},
		{
			name: 'Permission Handler',
			description: 'Manage device permissions',
			link: 'https://pub.dev/packages/permission_handler'
		},
		{
			name: 'Gal',
			description: 'Save images and videos to gallery',
			link: 'https://pub.dev/packages/gal'
		},
		{
			name: 'Flutter Dotenv',
			description: 'Environment variables management',
			link: 'https://pub.dev/packages/flutter_dotenv'
		},
		{
			name: 'Shared Preferences',
			description: 'Persistent storage for simple data',
			link: 'https://pub.dev/packages/shared_preferences'
		},
		{
			name: 'Back Button Interceptor',
			description: 'Handle back button press',
			link: 'https://pub.dev/packages/back_button_interceptor'
		},
		{
			name: 'Crypto',
			description: 'Cryptographic functions',
			link: 'https://pub.dev/packages/crypto'
		},
		{
			name: 'Path Provider',
			description: 'Find commonly used locations on the filesystem',
			link: 'https://pub.dev/packages/path_provider'
		}
	];
</script>

<svelte:head>
	<title>taeguncni info - isopng</title>
</svelte:head>

<div class="page">
	<div class="header">
		<div class="title">
			<span class="bracket">[</span>
			<span class="title-text">taeguncni info</span>
			<span class="bracket">]</span>
		</div>
		<div class="subtitle">technologies used in the app</div>
	</div>

	<div class="packages-section">
		{#each packages as pkg, index}
			<div class="package-item">
				<div class="package-header">
					<span class="package-number">[{index + 1}]</span>
					<span class="package-name">{pkg.name}</span>
				</div>
				<div class="package-description">{pkg.description}</div>
				<a href={pkg.link} target="_blank" rel="noopener noreferrer" class="package-link">
					<span class="link-arrow">→</span>
					<span class="link-text">{pkg.link}</span>
				</a>
			</div>
		{/each}
	</div>

	<div class="back-section">
		<a href="/taeguncni" class="back-link">
			<span class="back-arrow">&lt;-</span>
			<span class="back-text">back to taeguncni</span>
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
		gap: 60px;
	}

	.header {
		text-align: center;
		display: flex;
		flex-direction: column;
		gap: 12px;
	}

	.title {
		font-size: 24px;
		font-weight: normal;
		letter-spacing: 2px;
	}

	.subtitle {
		color: #666;
		font-size: 12px;
		letter-spacing: 1px;
		text-transform: lowercase;
	}

	.bracket {
		color: #666;
	}

	.title-text {
		color: #fff;
		margin: 0 8px;
	}

	.packages-section {
		width: 100%;
		max-width: 900px;
		display: flex;
		flex-direction: column;
		gap: 0;
	}

	.package-item {
		background: #000;
		border: 1px solid #222;
		border-bottom: none;
		padding: 20px 24px;
		display: flex;
		flex-direction: column;
		gap: 10px;
	}

	.package-item:last-child {
		border-bottom: 1px solid #222;
	}

	.package-item:hover {
		background: #0a0a0a;
		border-color: #333;
	}

	.package-header {
		display: flex;
		align-items: center;
		gap: 12px;
	}

	.package-number {
		color: #666;
		font-weight: bold;
		min-width: 35px;
		font-size: 13px;
	}

	.package-name {
		color: #fff;
		font-size: 14px;
		font-weight: bold;
		letter-spacing: 0.5px;
	}

	.package-description {
		color: #888;
		font-size: 12px;
		line-height: 1.5;
		margin-left: 47px;
		letter-spacing: 0.3px;
	}

	.package-link {
		display: flex;
		align-items: center;
		gap: 8px;
		margin-left: 47px;
		text-decoration: none;
		color: #555;
		font-size: 11px;
		letter-spacing: 0.3px;
		transition: color 0.2s;
		word-break: break-all;
	}

	.package-link:hover {
		color: #ff0000;
	}

	.link-arrow {
		color: inherit;
		min-width: 12px;
	}

	.link-text {
		color: inherit;
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
			gap: 40px;
		}

		.title {
			font-size: 20px;
		}

		.packages-section {
			max-width: 100%;
		}

		.package-item {
			padding: 16px 18px;
		}

		.package-number {
			font-size: 12px;
		}

		.package-name {
			font-size: 13px;
		}

		.package-description {
			font-size: 11px;
			margin-left: 40px;
		}

		.package-link {
			font-size: 10px;
			margin-left: 40px;
		}
	}
</style>