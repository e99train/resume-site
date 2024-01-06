<script>
  import Icon from "@iconify/svelte";
  import { colorScheme, Button, Grid } from "@svelteuidev/core";
  import NavLink from "./NavLink.svelte";

  function toggleTheme() {
    colorScheme.update((v) => (v === "light" ? "dark" : "light"));
  }
</script>

<div class="banner">
  <Grid align="center">
    <Grid.Col span={6} offset={0.5}
      ><p><b>Ethan Borsky</b> | <em> Software Developer</em></p></Grid.Col
    >
    <Grid.Col span={2} offset={2.5}>
      <nav>
        <NavLink href="/about-me" title="About Me" />
        <NavLink href="/resume" title="Resume" />
        <NavLink href="/projects" title="Projects" />
      </nav>
    </Grid.Col>
    <Grid.Col span={1}>
      <Button on:click={toggleTheme}>
        <Icon
          icon={$colorScheme === "light"
            ? "pixelarticons:moon"
            : "pixelarticons:sun-alt"}
        />
      </Button>
    </Grid.Col>
  </Grid>
</div>

<style lang="css">
  .banner {
    width: 100%;
    height: 100px;
    border: 5px solid coral;
  }
  nav {
    border: 5px solid cyan;
    display: flex;
    justify-content: space-between;
  }
  p {
    font-size: 2em;
  }
</style>
