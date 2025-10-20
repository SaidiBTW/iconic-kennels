<script lang="ts">
  import favicon from "$lib/assets/favicon.ico";
  import Navbar from "$lib/components/layout/Navbar.svelte";
  import "../app.css";

  let { children } = $props();
</script>

<svelte:head>
  <link rel="icon" href={favicon} />
</svelte:head>

<!-- App Layout -->
<div class="min-h-screen flex flex-col">
  <!-- ✅ Navbar appears on every page -->
  <Navbar />

  <!-- ✅ Render current route -->
  <main class="flex-1 container mx-auto py-8 mt-12">
    {@render children?.()}
  </main>
</div>
