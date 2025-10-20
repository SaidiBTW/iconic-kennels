<!-- This is the dogs page where we showcase the various dogs available for adoption or services. -->

<script lang="ts">
  // You can add any necessary imports or logic here
  import { onMount } from "svelte";

  interface Dog {
    name: string;
    age: number;
    description: string;
    image: string;
  }

  let dogs: Dog[] = [];

  onMount(() => {
    // Fetch dog data or define it here
    dogs = [
      {
        name: "Max",
        age: 3,
        description: "A friendly and energetic German Shepherd.",
        image: `https://picsum.photos/200/300?random=${Math.random()}`,
      },
      {
        name: "Bella",
        age: 2,
        description: "A loving and intelligent German Shepherd.",
        image: "https://picsum.photos/200/300?random=2",
      },
      {
        name: "Rocky",
        age: 4,
        description: "A loyal and protective German Shepherd.",
        image: "https://picsum.photos/200/300?random=3",
      },
      {
        name: "Rocky",
        age: 4,
        description: "A loyal and protective German Shepherd.",
        image: "https://picsum.photos/200/300?random=3",
      },
      {
        name: "Rocky",
        age: 4,
        description: "A loyal and protective German Shepherd.",
        image: "https://picsum.photos/200/300?random=3",
      },
      {
        name: "Rocky",
        age: 4,
        description: "A loyal and protective German Shepherd.",
        image: "https://picsum.photos/200/300?random=3",
      },
      {
        name: "Rocky",
        age: 4,
        description: "A loyal and protective German Shepherd.",
        image: "https://picsum.photos/200/300?random=3",
      },
      {
        name: "Rocky",
        age: 4,
        description: "A loyal and protective German Shepherd.",
        image: "https://picsum.photos/200/300?random=3",
      },
      {
        name: "Rocky",
        age: 4,
        description: "A loyal and protective German Shepherd.",
        image: "https://picsum.photos/200/300?random=3",
      },
      {
        name: "Rocky",
        age: 4,
        description: "A loyal and protective German Shepherd.",
        image: "https://picsum.photos/200/300?random=3",
      },
    ];
  });
</script>

<h1 class="text-3xl font-bold mb-4">Our Dogs</h1>
<p class="mb-4"></p>
<!-- Masonry-style layout -->
<div class="columns-2 md:columns-3 lg:columns-4 gap-4 p-4">
  {#each dogs as item}
    <div class="mb-4 break-inside-avoid">
      <img
        src={item.image}
        alt={item.name}
        class="w-full rounded-lg object-cover"
      />
      <p class="mt-2 text-sm font-medium text-gray-700">{item.name}</p>
    </div>
  {/each}
</div>
