<script>
  import Icon from "@iconify/svelte";
  import { colorScheme, Button, Grid } from "@svelteuidev/core";

  function toggleTheme() {
    colorScheme.update((v) => (v === "light" ? "dark" : "light"));
  }
</script>

<div class="banner">
  <Grid>
    <Grid.Col span={10} offset={1}><h1>Ethan Borsky</h1></Grid.Col>
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
    height: 20%;
  }

  h1 {
    text-align: center;
  }
</style>
