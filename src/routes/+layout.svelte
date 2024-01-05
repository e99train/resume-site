<script>
  import Banner from "$lib/banner.svelte";
  import { SvelteUIProvider, colorScheme } from "@svelteuidev/core";
</script>

<SvelteUIProvider
  withNormalizeCSS
  withGlobalStyles
  themeObserver={$colorScheme}
>
  <Banner />
  <slot />
</SvelteUIProvider>
