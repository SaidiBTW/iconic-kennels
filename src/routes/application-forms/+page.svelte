<script lang="ts">
  const forms = [
    {
      title: "Puppy Adoption",
      description:
        "Apply to adopt one of our adorable German Shepherd puppies.",
      link: "/application-forms/puppy-adoption-form",
      color: "bg-blue-100 text-blue-800",
    },
    {
      title: "Adult Adoption",
      description: "Find your perfect adult German Shepherd companion.",
      link: "/application-forms/german-shepherd-adoption-form",
      color: "bg-green-100 text-green-800",
    },
    {
      title: "Stud Service",
      description: "Apply for our professional German Shepherd stud services.",
      link: "/application-forms/german-shepherd-stud-form",
      color: "bg-yellow-100 text-yellow-800",
    },
  ];
</script>

<section class="max-w-5xl mx-auto px-4 py-12">
  <h1 class="text-4xl font-bold text-center font-['Playfair_Display'] mb-4">
    Application Forms
  </h1>
  <p class="text-center text-gray-600 mb-10">
    Please select an application form below to begin.
  </p>

  <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
    {#each forms as form}
      <div
        class="bg-white rounded-2xl shadow-sm hover:shadow-md transition p-6 flex flex-col items-center text-center"
      >
        <div
          class={`w-16 h-16 flex items-center justify-center rounded-full mb-4 ${form.color}`}
        >
          <!-- Simple icon placeholder; you can replace with lucide or heroicons -->
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-8 h-8"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M16.5 10.5V6.75a4.5 4.5 0 00-9 0v3.75m11.25 0a2.25 2.25 0 012.25 2.25v6.75a2.25 2.25 0 01-2.25 2.25H5.25A2.25 2.25 0 013 19.5v-6.75a2.25 2.25 0 012.25-2.25m11.25 0H5.25"
            />
          </svg>
        </div>

        <h2 class="text-xl font-semibold mb-2">{form.title}</h2>
        <p class="text-gray-600 text-sm mb-4">{form.description}</p>

        <a
          href={form.link}
          class="mt-auto inline-block w-full py-2 px-4 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition"
        >
          Fill Out Form
        </a>
      </div>
    {/each}
  </div>
</section>
