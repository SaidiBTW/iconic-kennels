<script lang="ts">
  import { page } from "$app/stores";
  import logo from "$lib/assets/logo.png";
  import { derived } from "svelte/store";
  let menuOpen = false;

  const currentPath = derived(page, ($page) => $page.url.pathname);

  const links = [
    { name: "Home", href: "/" },
    { name: "About", href: "/about" },
    { name: "Dogs", href: "/dogs" },
    { name: "Our Services", href: "/services" },
    { name: "FAQ", href: "/faq" },
    { name: "Application Forms", href: "/application-forms" },
  ];
</script>

<nav class="bg-white border-b border-gray-200">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between h-16 items-center">
      <!-- Desktop Links -->
      <!--Show Logo from asset folder-->
      <div class="hidden md:flex items-center">
        <img src={logo} alt="Iconic Kennels Logo" class="h-8 w-8 mr-2" />
        <span class="text-xl font-bold text-gray-800">Iconic Kennels</span>
      </div>
      <div class="hidden md:flex space-x-8">
        {#each links as link}
          <a
            href={link.href}
            class="text-gray-600 hover:text-gray-900 font-medium"
            class:underline={$currentPath === link.href}
          >
            {link.name}
          </a>
        {/each}
      </div>

      <!-- Mobile Menu Button -->
      <button
        type="button"
        class="md:hidden text-gray-600 hover:text-gray-900 focus:outline-none"
        on:click={() => (menuOpen = !menuOpen)}
        aria-label={menuOpen ? "Close menu" : "Open menu"}
        aria-expanded={menuOpen}
      >
        <svg
          class="h-6 w-6"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d={menuOpen
              ? "M6 18L18 6M6 6l12 12" // X icon
              : "M4 6h16M4 12h16M4 18h16"}
          />
        </svg>
      </button>
    </div>
  </div>

  <!-- Mobile Links -->
  {#if menuOpen}
    <div class="md:hidden px-4 pb-3 space-y-1 border-t border-gray-200">
      {#each links as link}
        <a
          href={link.href}
          class="block py-2 text-gray-700 hover:text-gray-900 font-medium"
          class:underline={$currentPath === link.href}
          on:click={() => (menuOpen = false)}
        >
          {link.name}
        </a>
      {/each}
    </div>
  {/if}
</nav>
