<script lang="ts">
  import { onMount } from "svelte";

  interface GalleryItem {
    src: string;
    caption?: string;
    category: "puppy" | "adult" | "show" | "video";
  }

  let gallery: GalleryItem[] = [];

  onMount(() => {
    gallery = [
      {
        src: "https://images.unsplash.com/photo-1601758123927-198d0481c574",
        caption: "Litter A - 2 Weeks Old",
        category: "puppy",
      },
      {
        src: "https://images.unsplash.com/photo-1558788353-f76d92427f16",
        caption: "Litter B - 6 Weeks Old",
        category: "puppy",
      },
      {
        src: "https://images.unsplash.com/photo-1560807707-8cc77767d783",
        caption: "Adult - Long Coat",
        category: "adult",
      },
      {
        src: "https://images.unsplash.com/photo-1619983081563-430f636f26c5",
        caption: "Adult - Short Coat",
        category: "adult",
      },
      {
        src: "https://images.unsplash.com/photo-1548199973-03cce0bbc87b",
        caption: "Champion Lineup",
        category: "show",
      },
      {
        src: "https://images.unsplash.com/photo-1525253086316-d0c936c814f8",
        caption: "Best in Show",
        category: "show",
      },
      {
        src: "https://images.unsplash.com/photo-1574158622682-e40e69881006",
        caption: "Training Session",
        category: "video",
      },
      {
        src: "https://images.unsplash.com/photo-1518717758536-85ae29035b6d",
        caption: "Outdoor Playtime",
        category: "video",
      },
    ];
  });
</script>

<section class="max-w-7xl mx-auto py-20 px-6">
  <div class="text-center mb-16">
    <h1
      class="text-4xl md:text-5xl font-bold mb-4 tracking-tight text-gray-900"
    >
      Our Gallery
    </h1>
    <p class="text-lg text-gray-600 max-w-2xl mx-auto">
      Explore our world of adorable puppies, champion adults, and training
      highlights.
    </p>
  </div>

  {#each ["puppy", "adult", "show", "video"] as section}
    <div class="mb-20">
      <h2 class="text-2xl md:text-3xl font-semibold mb-6 flex items-center">
        <span class="border-l-4 border-amber-600 pl-4 capitalize"
          >{section} Gallery</span
        >
      </h2>

      <div
        class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8"
      >
        {#each gallery.filter((i) => i.category === section) as item}
          <div
            class="group relative rounded-2xl overflow-hidden shadow-md hover:shadow-xl transition-all duration-300 bg-white"
          >
            <img
              src={item.src}
              alt={item.caption}
              class="w-full h-64 object-cover group-hover:scale-105 transition-transform duration-500"
              loading="lazy"
            />

            {#if section === "video"}
              <div
                class="absolute inset-0 bg-black/40 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity duration-300"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-16 w-16 text-white"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M14.752 11.168l-4.596-2.65A1 1 0 009 9.35v5.3a1 1 0 001.156.832l4.596-2.65a1 1 0 000-1.664z"
                  />
                </svg>
              </div>
            {/if}

            <div
              class="absolute bottom-0 w-full bg-gradient-to-t from-black/70 to-transparent p-4"
            >
              <p class="text-white text-sm font-medium">{item.caption}</p>
            </div>
          </div>
        {/each}
      </div>
    </div>
  {/each}

  <div class="text-center py-16 border-t border-gray-200 mt-20">
    <h2 class="text-2xl md:text-3xl font-semibold mb-4 text-gray-900">
      Follow Us on Instagram
    </h2>
    <p class="text-gray-600 mb-8 max-w-md mx-auto">
      See more adorable updates from our kennel and puppy litters.
    </p>
    <a
      href="https://www.instagram.com"
      target="_blank"
      rel="noopener noreferrer"
      class="inline-flex items-center gap-2 bg-black text-white hover:bg-gray-800 px-6 py-3 rounded-lg font-medium transition-colors duration-200"
    >
      View Instagram Gallery
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="h-5 w-5"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M17 8l4 4m0 0l-4 4m4-4H3"
        />
      </svg>
    </a>
  </div>
</section>
