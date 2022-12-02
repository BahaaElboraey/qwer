<script>
  import "@skeletonlabs/skeleton/themes/theme-skeleton.css";
  import "@skeletonlabs/skeleton/styles/all.css";
  import "../app.postcss";
  import { AppShell, AppBar, GradientHeading } from "@skeletonlabs/skeleton";
  import { LightSwitch, Avatar } from "@skeletonlabs/skeleton";
  import { menu } from "@skeletonlabs/skeleton";
</script>

<!-- svelte-ignore security-anchor-rel-noreferrer -->
<AppShell>
  <svelte:fragment slot="header">
    <!-- Insert the App Bar: -->
    <AppBar class="p-2 md:p-3">
      <svelte:fragment slot="lead">
        <span class="relative md:hidden">
          <button
            class="btn p-0 mr-3"
            use:menu={{ menu: "example", interactive: true }}
          >
            <svg viewBox="0 0 100 60" width="20" height="20">
              <rect width="100" height="20" />
              <rect y="30" width="100" height="20" />
              <rect y="60" width="100" height="20" />
            </svg></button
          >

          <nav class="list-nav card p-4 w-64 shadow-xl bg-opacity-80 dark:bg-opacity-80 hover:bg-opacity-100 dark:hover:bg-opacity-100" data-menu="example">
            <ul>
              <li><a href="/">Dashboard</a></li>
              <li><a href="/">Loveds</a></li>
              <li><a href="/">Blog</a></li>
            </ul>
          </nav>
        </span>

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
          class="pt-4 btn btn-base hover:bg-slate-400 dark:hover:bg-green-300 rounded-3xl ml-3 dark:hover:text-black p-3.5 md:py-5 hover:font-bold hidden md:inline-block"
          >Dashboard</a
        >
        <a
          href="/"
          class="pt-4 btn btn-base hover:bg-slate-400 dark:hover:bg-green-300 rounded-3xl ml-3 dark:hover:text-black p-3.5 md:py-5 hover:font-bold hidden md:inline-block"
          >Loveds</a
        >
        <a
          href="/"
          class="pt-4 btn btn-base hover:bg-slate-400 dark:hover:bg-green-300 rounded-3xl ml-3 dark:hover:text-black p-3.5 md:py-5 hover:font-bold hidden md:inline-block"
          >About</a
        >
      </svelte:fragment>

      <svelte:fragment slot="trail">
        <LightSwitch />
        <Avatar
          width="w-10"
          border="border-2 hover:border-slate-700 dark:hover:border-lime-400"
        
          />
      </svelte:fragment>
    </AppBar>

    <!-- --- -->
  </svelte:fragment>
  <svelte:fragment slot="pageHeader" />
  <!-- Router Slot -->
  <slot />

  <svelte:fragment slot="footer">Footer</svelte:fragment>
</AppShell>
