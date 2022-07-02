<script lang="ts">
  import '../app.css';
  import Navbar from '$lib/Navbar/index.svelte';
</script>

<Navbar />

<main>
  <slot />
</main>

<footer>
  <p>visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit</p>
</footer>
