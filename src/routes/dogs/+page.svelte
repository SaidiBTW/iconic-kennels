<script lang="ts">
  import { onMount } from "svelte";

  interface Dog {
    name: string;
    age: number;
    description: string;
    image: string;
    category: "Sire" | "Dam" | "Champion";
    achievements?: string[];
    pedigreeLink?: string;
  }

  let dogs: Dog[] = [];

  onMount(() => {
    dogs = [
      {
        name: "Max",
        age: 4,
        category: "Sire",
        description:
          "Strong, intelligent, and confident stud with an excellent lineage.",
        image: "https://picsum.photos/400/400?random=1",
        pedigreeLink: "#",
      },
      {
        name: "Thor",
        age: 5,
        category: "Sire",
        description: "Award-winning male with excellent drive and temperament.",
        image: "https://picsum.photos/400/400?random=2",
        pedigreeLink: "#",
      },
      {
        name: "Bella",
        age: 3,
        category: "Dam",
        description:
          "Gentle and protective dam known for her nurturing litters.",
        image: "https://picsum.photos/400/400?random=3",
        pedigreeLink: "#",
      },
      {
        name: "Luna",
        age: 2,
        category: "Dam",
        description:
          "Active and alert female, mother to multiple healthy litters.",
        image: "https://picsum.photos/400/400?random=4",
        pedigreeLink: "#",
      },
      {
        name: "Rex",
        age: 5,
        category: "Champion",
        description:
          "EAKC Champion 2024 – praised for structure and obedience.",
        image: "https://picsum.photos/400/400?random=5",
        achievements: [
          "EAKC Champion 2024",
          "Best of Breed – Nairobi Show",
          "Judge’s Critique: Excellent structure and confidence",
        ],
      },
      {
        name: "Zara",
        age: 3,
        category: "Champion",
        description: "National Champion – admired for poise and performance.",
        image: "https://picsum.photos/400/400?random=6",
        achievements: [
          "Champion Class Winner – 2023",
          "Judge’s Critique: Excellent movement and alert expression",
        ],
      },
    ];
  });

  const categories = ["Sire", "Dam", "Champion"];
</script>

<!-- Page Header -->
<section class="max-w-6xl mx-auto px-6 py-16">
  <h1
    class="text-4xl md:text-5xl font-bold font-[Playfair_Display] text-center text-gray-900 mb-6"
  >
    Our Dogs
  </h1>
  <p class="text-center text-gray-600 max-w-2xl mx-auto leading-relaxed mb-16">
    Meet our exceptional German Shepherds — sires, dams, and champions raised
    with care, discipline, and dedication.
  </p>

  {#each categories as category}
    <div class="mb-20">
      <!-- Category Heading -->
      <div class="flex items-center mb-10">
        <div class="h-8 w-1 bg-black rounded-full mr-3"></div>
        <h2 class="text-2xl md:text-3xl font-semibold text-gray-900">
          {category === "Sire"
            ? "Sires (Male Breeding Dogs)"
            : category === "Dam"
              ? "Dams (Female Breeding Dogs)"
              : "Champions & Show Stars"}
        </h2>
      </div>

      <!-- Dog Cards Grid -->
      <div
        class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 place-items-center"
      >
        {#each dogs.filter((d) => d.category === category) as dog}
          <div
            class="bg-white rounded-2xl shadow-sm hover:shadow-lg transition-shadow duration-300 flex flex-col w-full max-w-sm"
          >
            <div class="relative">
              <img
                src={dog.image}
                alt={dog.name}
                class="rounded-t-2xl object-cover w-full h-64"
              />
              <div
                class="absolute bottom-0 bg-gradient-to-t from-black/60 to-transparent text-white p-4 w-full rounded-b-2xl"
              >
                <h3 class="text-lg font-semibold">{dog.name}</h3>
                <p class="text-sm opacity-90">Age: {dog.age} years</p>
              </div>
            </div>

            <div class="p-5 flex-1 flex flex-col">
              <p class="text-gray-700 text-sm leading-relaxed mb-3">
                {dog.description}
              </p>

              {#if dog.achievements}
                <ul
                  class="text-sm text-gray-600 list-disc list-inside mb-4 space-y-1"
                >
                  {#each dog.achievements as a}
                    <li>{a}</li>
                  {/each}
                </ul>
              {/if}

              {#if dog.pedigreeLink}
                <a
                  href={dog.pedigreeLink}
                  class="mt-auto inline-block text-center bg-black text-white py-2 rounded-lg hover:bg-gray-800 transition-colors"
                >
                  View Pedigree
                </a>
              {/if}
            </div>
          </div>
        {/each}
      </div>
    </div>
  {/each}
</section>

<style>
  h1,
  h2 {
    scroll-margin-top: 6rem;
  }
</style>
