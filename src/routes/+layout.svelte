<script>
	import '../app.css';
</script>

<div class="bg-slate-900">
	<header class="bg-slate-900 text-white shadow-md" style="position: sticky; top: 0;">
		<nav
			class="mx-auto flex max-w-7xl items-center justify-between p-6 lg:px-8"
			aria-label="Global"
		>
			<a class="text-xl" href="/">Reiseplaner</a>
			<div class="flex gap-x-12 text-md">
				<a href="/security">Security</a>
				<a href="/blog">Blog</a>
				<a href="/careers">Careers</a>
			</div>
			<a class="text-xl" href="/sales">Contact Sales</a>
		</nav>
	</header>

	<main class="text-white flex-grow h-screen flex items-center justify-center">
		<div class="mx-auto max-w-5xl" style="position: sticky; top: 90px; margin-top: 20px;">
			<slot />
		</div>
	</main>

	<footer class="bg-slate-900 text-white shadow-md text-md fixed bottom-0 left-0 w-full">
		<nav class="mx-auto flex max-w-7xl items-center justify-center p-6 lg:px-8" aria-label="Global">
			<div class="flex gap-7">
				<a href="/security">Security</a>
				<a href="/blog">Blog</a>
				<a href="/careers">Careers</a>
				<a href="/legal">Legal</a>
			</div>
		</nav>
	</footer>
</div>
