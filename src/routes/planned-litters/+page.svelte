<script lang="ts">
  // In the future, you can replace this static data with an API call
  import dog1 from "$lib/assets/dog1.jpeg";
  import dog2 from "$lib/assets/dog2.jpeg";
  import dog3 from "$lib/assets/dog3.jpeg";
  import { onMount } from "svelte";

  var litters: any[] = [];

  onMount(() => {
    litters = [
      {
        id: 1,
        sire: "Titan von Iconic",
        dam: "Luna von Blackridge",
        expected: "November 2025",
        status: "Accepting Applications",
        image: { dog1 },
        from: "from-blue-600",
        to: "to-indigo-400",
      },
      {
        id: 2,
        sire: "Rex von Iconic",
        dam: "Zara vom Haus",
        expected: "January 2026",
        status: "Upcoming",
        image: { dog2 },
        from: "from-amber-500",
        to: "to-orange-400",
      },
      {
        id: 3,
        sire: "Max von Regal",
        dam: "Nova von Iconic",
        expected: "March 2026",
        status: "Planned",
        image: { dog3 },
        from: "from-emerald-600",
        to: "to-teal-400",
      },
    ];
  });
</script>

<section class="max-w-6xl mx-auto px-4 py-16">
  <h1 class="text-4xl font-bold text-center mb-4 text-gray-900">
    Planned Litters
  </h1>
  <p class="text-center text-gray-600 mb-12">
    Explore our upcoming German Shepherd litters. Reserve early to secure your
    puppy from champion bloodlines.
  </p>

  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
    {#each litters as litter}
      <div
        class="group bg-white/60 backdrop-blur-lg rounded-3xl border border-gray-200 shadow-sm hover:shadow-lg hover:-translate-y-1 transition-all duration-300 overflow-hidden flex flex-col"
      >
        <div class="relative w-full h-56 overflow-hidden">
          <img
            src="https://picsum.photos/400/300"
            alt={`${litter.sire} × ${litter.dam}`}
            class="object-cover w-full h-full group-hover:scale-105 transition-transform duration-300"
          />
          <div
            class={`absolute top-4 left-4 px-3 py-1.5 text-sm font-medium rounded-full bg-gradient-to-br ${litter.from} ${litter.to} text-white shadow-md`}
          >
            {litter.status}
          </div>
        </div>

        <div class="flex-1 flex flex-col p-6 text-center">
          <h2 class="text-xl font-semibold text-gray-900 mb-2">
            {litter.sire} × {litter.dam}
          </h2>
          <p class="text-gray-600 mb-4">Expected: {litter.expected}</p>

          <a
            href="/application-forms/puppy-adoption-form"
            class="mt-auto inline-block py-3 px-6 bg-gray-900 text-white rounded-xl hover:bg-gray-800 transition font-medium tracking-wide"
          >
            Apply Now
          </a>
        </div>
      </div>
    {/each}
  </div>
</section>
