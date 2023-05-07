<script>
	import { Cloudinary } from '@cloudinary/url-gen';

	const cld = new Cloudinary({
		cloud: {
			cloudName: 'tutorials'
		}
	});

	const myImage = cld.image('cld-sample-5');
	myImage.format('auto').quality('auto');
</script>

<main class="main">
	<div class="container">
		<h1 class="title">SvelteKit &amp; Cloudinary Client SDK</h1>
	</div>

	<div class="container">
		<div>
			<h2>Auto format, Auto Quality</h2>
			<img src={myImage.toURL()} alt="from cloudinary" width={300} />
		</div>
	</div>

	<div class="container">
		<h2>Resources</h2>
		<p>
			<a
				href="https://github.com/colbyfayock/cloudinary-examples/tree/main/examples/sveltekit-client-sdk"
				>See the code on github.com.</a
			>
		</p>
	</div>
</main>

<style>
	.container {
		width: 100%;
		max-width: 1024px;
		padding: 0 1em;
		margin: 0 auto;
		display: flex;
		align-items: center;
	}

	.title {
		text-align: center;
		margin: 2em 0;
	}
</style>
