<script lang="ts">
  const forms = [
    {
      title: "Puppy Adoption",
      description:
        "Apply to adopt one of our adorable German Shepherd puppies.",
      link: "/application-forms/puppy-adoption-form",
    },
    {
      title: "Adult Adoption",
      description: "Find your perfect adult German Shepherd companion.",
      link: "/application-forms/german-shepherd-adoption-form",
    },
    {
      title: "Stud Service",
      description: "Apply for our professional German Shepherd stud services.",
      link: "/application-forms/german-shepherd-stud-form",
    },
  ];
</script>

<section class="max-w-5xl mx-auto px-4 py-12">
  <h1 class="text-4xl font-bold text-center mb-4">Application Forms</h1>
  <p class="text-center text-gray-600 mb-10">
    Please select an application form below to begin.
  </p>

  <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
    {#each forms as form}
      <div
        class="group bg-white/60 backdrop-blur-lg p-8 rounded-3xl border border-gray-200 shadow-sm hover:shadow-lg hover:-translate-y-1 transition-all duration-300 flex flex-col items-center text-center"
      >
        <!-- Gradient icon container -->
        <div
          class="flex items-center justify-center w-16 h-16 rounded-2xl bg-gradient-to-br from-gray-900 to-gray-700 text-white shadow-md group-hover:scale-110 transition-transform duration-300 mb-4"
        >
          <!-- Replace with lucide or heroicons if desired -->
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

        <h2 class="text-xl font-semibold text-gray-900 mb-2">{form.title}</h2>
        <p class="text-gray-600 text-sm mb-6">{form.description}</p>

        <a
          href={form.link}
          class="mt-auto inline-block w-full py-2 px-4 bg-gray-900 text-white rounded-lg hover:bg-gray-800 transition-colors duration-200"
        >
          Fill Out Form
        </a>
      </div>
    {/each}
  </div>
</section>
