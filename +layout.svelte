<script>
	import '@brainandbones/skeleton/themes/theme-skeleton.css';
	import '@brainandbones/skeleton/styles/all.css';
	import '../app.postcss';
	import { AppShell, AppBar, GradientHeading } from '@brainandbones/skeleton';
	import { LightSwitch, Avatar } from '@brainandbones/skeleton';
</script>

<!-- svelte-ignore security-anchor-rel-noreferrer -->
<AppShell>
	<svelte:fragment slot="header">
		<!-- Insert the App Bar: -->
		<AppBar>
			<svelte:fragment slot="lead">
				<div class=" md:hidden">
					<button class="btn p-0 mr-3">
						<svg viewBox="0 0 100 60" width="20" height="20">
							<rect width="100" height="20" />
							<rect y="30" width="100" height="20" />
							<rect y="60" width="100" height="20" />
						</svg></button
					>
				</div>
				<a href="/">
					<GradientHeading
						tag="h1"
						direction="bg-gradient-to-br"
						from="from-primary-500"
						to="to-accent-500"
					>
						Elkheir.com
					</GradientHeading>
				</a>
				<a
					href="/"
					class="pt-4 btn btn-base hover:bg-slate-400 dark:hover:bg-green-300 rounded-3xl ml-3 dark:hover:text-black p-3.5 md:py-5 hover:font-bold "
					>Dashboard</a
				>
				<a
					href="/"
					class="pt-4 btn btn-base hover:bg-slate-400 dark:hover:bg-green-300 rounded-3xl ml-3 dark:hover:text-black p-3.5 md:py-5 hover:font-bold "
					>Loveds</a
				>
				<a
				href="/"
				class="pt-4 btn btn-base hover:bg-slate-400 dark:hover:bg-green-300 rounded-3xl ml-3 dark:hover:text-black p-3.5 md:py-5 hover:font-bold "
				>About</a
				>
			</svelte:fragment>

			<svelte:fragment slot="trail">
				<LightSwitch />
				<Avatar width="w-10" border="border-4 hover:border-lime-300 dark:hover:" />
			</svelte:fragment>
		</AppBar>

		<!-- --- -->
	</svelte:fragment>
	<svelte:fragment slot="pageHeader" />
	<!-- Router Slot -->
	<slot />

	<svelte:fragment slot="footer">Footer</svelte:fragment>
</AppShell>
