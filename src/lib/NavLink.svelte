<script>
  import { page } from "$app/stores";
  import { Button } from "@svelteuidev/core";
  import { onMount } from "svelte";

  let currentPath;
  onMount(() => {
    currentPath = window.location.pathname;
  });
  /**
   * @type {String}
   */
  export let title;
  /**
   * @type {String}
   */
  export let href;
</script>

<!-- <a {href} class:active={$page.url.pathname.includes(href)}> -->
<!--   {title} -->
<!-- </a> -->

<Button
  ripple
  {href}
  color={$page.url.pathname.includes(href) ? "cyan" : "gray"}>{title}</Button
>

<style>
  /* Button.active { */
  /*   color: gray; */
  /* } */
  /* a { */
  /*   text-decoration: none; */
  /* } */
</style>
