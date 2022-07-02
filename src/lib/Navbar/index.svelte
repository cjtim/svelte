<script lang="ts">
  import Logo from './_Logo.svelte';
  import Mobile from './_MobileItems.svelte';
  import Profile from './_Profile.svelte';
  import type { NavbarItem } from 'src/interfaces/navbar';
  import Notification from './_Notification.svelte';

  const items: NavbarItem[] = [
    {
      title: 'Home',
      path: '/'
    },
    {
      title: 'Todos',
      path: '/todos'
    }
  ];
</script>

<header>
  <nav class="bg-gray-800">
    <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
      <div class="relative flex items-center justify-between h-16">
        <Logo {items} />
        <div
          class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0"
        >
          <Notification />
          <Profile />
        </div>
      </div>
    </div>

    <!-- Mobile menu, show/hide based on menu state. -->
    <Mobile {items} />
  </nav>

  <div class="corner">
    <!-- TODO put something else here? github link? -->
  </div>
</header>
