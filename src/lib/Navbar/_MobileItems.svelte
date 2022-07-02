<script lang="ts">
  import { page } from '$app/stores';
  import type { NavbarItem } from 'src/interfaces/navbar';
  const btnBaseCss = 'block px-3 py-2 rounded-md text-base font-medium';
  const unhoverCss = 'text-gray-300 hover:bg-gray-700 hover:text-white ' + btnBaseCss;
  const hoverCss = 'bg-gray-900 text-white ' + btnBaseCss;

  export let items: NavbarItem[];
</script>

<div class="sm:hidden" id="mobile-menu">
  <div class="px-2 pt-2 pb-3 space-y-1">
    {#each items as item}
      <a
        href={item.path}
        class={$page.url.pathname === item.path ? hoverCss : unhoverCss}
        aria-current="page"
        >{item.title}
      </a>
    {/each}
  </div>
</div>
