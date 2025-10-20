<script lang="ts">
  import { page } from "$app/stores"; // keep your current import
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

<nav
  class="fixed top-0 left-0 w-full bg-white/70 backdrop-blur-md border-b border-gray-200 z-50"
>
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between items-center h-16">
      <!-- Logo -->
      <a href="/" class="flex items-center space-x-2">
        <img src={logo} alt="Iconic Kennels Logo" class="h-10 w-auto" />
        <span
          class="text-lg sm:text-xl font-semibold text-gray-800 tracking-tight"
        >
          Iconic Kennels
        </span>
      </a>

      <!-- Desktop Navigation -->
      <div class="hidden md:flex items-center space-x-8">
        {#each links as link}
          <a
            href={link.href}
            class="relative font-medium transition-colors duration-200
                   text-gray-600 hover:text-gray-900"
          >
            <span class={$currentPath === link.href ? "text-gray-900" : ""}
              >{link.name}</span
            >
            <span
              class="absolute left-0 -bottom-1 h-0.5 bg-gray-900 transition-all duration-300"
              class:w-full={$currentPath === link.href}
              class:w-0={$currentPath !== link.href}
            ></span>
          </a>
        {/each}
      </div>

      <!-- Mobile Menu Button -->
      <button
        class="md:hidden relative z-50 p-2 text-gray-700 focus:outline-none"
        on:click={() => (menuOpen = !menuOpen)}
        aria-label={menuOpen ? "Close menu" : "Open menu"}
      >
        <div class="w-6 h-6 flex flex-col justify-between">
          <span
            class="block h-0.5 bg-gray-800 transition-transform duration-300"
            class:rotate-45={menuOpen}
            class:translate-y-[6px]={menuOpen}
          ></span>
          <span
            class="block h-0.5 bg-gray-800 transition-opacity duration-300"
            class:opacity-0={menuOpen}
          ></span>
          <span
            class="block h-0.5 bg-gray-800 transition-transform duration-300"
            class:-rotate-45={menuOpen}
            class:-translate-y-[6px]={menuOpen}
          ></span>
        </div>
      </button>
    </div>
  </div>

  <!-- Mobile Dropdown -->
  <div
    class="md:hidden overflow-hidden transition-[max-height,opacity] duration-500 bg-white/95 backdrop-blur-md border-t border-gray-200 shadow-md"
    style:max-height={menuOpen ? "500px" : "0px"}
    style:opacity={menuOpen ? "1" : "0"}
  >
    <div class="px-6 py-4 space-y-4">
      {#each links as link}
        <a
          href={link.href}
          on:click={() => (menuOpen = false)}
          class="block text-base font-medium text-gray-700 hover:text-gray-900 transition"
        >
          {link.name}
        </a>
      {/each}
    </div>
  </div>
</nav>
