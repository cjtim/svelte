<script lang="ts">
  import { spring } from 'svelte/motion';

  let show = false;

  const displayed_show = spring();
  $: displayed_show.set(show);

  const toggle = () => {
    show = !show;
  };
</script>

<div class="ml-3 relative">
  <div>
    <button
      type="button"
      class="bg-gray-800 flex text-sm rounded-full focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-800 focus:ring-white"
      id="user-menu-button"
      aria-expanded="false"
      aria-haspopup="true"
      on:click={toggle}
    >
      <span class="sr-only">Open user menu</span>
      <img
        class="h-8 w-8 rounded-full"
        src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
        alt=""
      />
    </button>
  </div>
  <div
    class="origin-top-right absolute right-0 mt-2 w-48 rounded-md shadow-lg py-1 bg-white ring-1 ring-black ring-opacity-5 focus:outline-none"
    role="menu"
    aria-orientation="vertical"
    aria-labelledby="user-menu-button"
    tabindex="-1"
    hidden={!show}
  >
    <a
      href="/#"
      class="block px-4 py-2 text-sm text-gray-700"
      role="menuitem"
      tabindex="-1"
      id="user-menu-item-0">Your Profile</a
    >
    <a
      href="/#"
      class="block px-4 py-2 text-sm text-gray-700"
      role="menuitem"
      tabindex="-1"
      id="user-menu-item-1">Settings</a
    >
    <a
      href="/#"
      class="block px-4 py-2 text-sm text-gray-700"
      role="menuitem"
      tabindex="-1"
      id="user-menu-item-2">Sign out</a
    >
  </div>
</div>
