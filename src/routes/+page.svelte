<!-- <script> -->
<!--   import AboutMe from "$lib/about-me.svelte"; -->
<!--   import Projects from "$lib/projects.svelte"; -->
<!--   import Resume from "$lib/resume.svelte"; -->
<!--   import { Tabs } from "@svelteuidev/core"; -->
<!-- </script> -->
<!---->
<!-- <Tabs grow variant="outline" position="center"> -->
<!--   <Tabs.Tab label="About Me"> -->
<!--     <AboutMe /> -->
<!--   </Tabs.Tab> -->
<!--   <Tabs.Tab label="Resume"> -->
<!--     <Resume /> -->
<!--   </Tabs.Tab> -->
<!--   <Tabs.Tab label="Projects"> -->
<!--     <Projects /> -->
<!--   </Tabs.Tab> -->
<!-- </Tabs> -->
<script>
  import { browser } from "$app/environment";

  if (browser) {
    window.location.href = "/about-me";
  }
</script>

<p>This is the page</p>
