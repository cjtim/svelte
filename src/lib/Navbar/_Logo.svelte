<script lang="ts">
  import type { NavbarItem } from 'src/interfaces/navbar';

  import DesktopItems from './_DesktopItems.svelte';

  export let items: NavbarItem[];
</script>

<div class="flex-1 flex items-center justify-center sm:items-stretch sm:justify-start">
  <div class="flex-shrink-0 flex items-center">
    <img
      class="block lg:hidden h-8 w-auto"
      src="https://tailwindui.com/img/logos/workflow-mark-indigo-500.svg"
      alt="Workflow"
    />
    <img
      class="hidden lg:block h-8 w-auto"
      src="https://tailwindui.com/img/logos/workflow-logo-indigo-500-mark-white-text.svg"
      alt="Workflow"
    />
  </div>
  <DesktopItems {items} />
</div>
