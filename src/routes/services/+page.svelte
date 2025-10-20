<script>
  import dog1 from "$lib/assets/dog1.jpeg";
  import dog2 from "$lib/assets/dog2.jpeg";
  import dog3 from "$lib/assets/dog3.jpeg";
  import {
    Camera,
    Dog,
    HeartHandshake,
    PawPrint,
    ShieldCheck,
  } from "@lucide/svelte";
</script>

<div class="max-w-7xl mx-auto px-6 py-20 space-y-28 text-gray-800">
  <!-- HERO -->
  <section class="text-center space-y-5">
    <h1
      class="text-5xl md:text-6xl font-bold font-['Playfair_Display'] text-gray-900 tracking-tight"
    >
      Our Services
    </h1>
    <p class="text-lg text-gray-600 max-w-2xl mx-auto leading-relaxed">
      Beyond breeding — we offer lifelong care, training, and companionship
      services tailored to help your German Shepherd thrive in every stage of
      life.
    </p>
  </section>

  <!-- SERVICES GRID -->
  <section class="grid sm:grid-cols-2 lg:grid-cols-3 gap-10">
    {#each [{ icon: PawPrint, title: "Premium Breeding", desc: "Selective breeding focused on health, temperament, and lineage excellence." }, { icon: Dog, title: "Training & Obedience", desc: "Build discipline and connection through tailored training programs." }, { icon: HeartHandshake, title: "Adoption & Pairing", desc: "Thoughtful pairing to match each family with the perfect companion." }, { icon: ShieldCheck, title: "Boarding & Care", desc: "A safe, loving environment for your dog with round-the-clock attention." }, { icon: Camera, title: "Pet Photography", desc: "Professional sessions to capture your dog's best moments." }, { icon: PawPrint, title: "Health & Nutrition", desc: "Comprehensive guidance on diet, wellness, and preventive care." }] as service}
      <div
        class="group bg-white/60 backdrop-blur-lg p-8 rounded-3xl border border-gray-200 shadow-sm hover:shadow-lg hover:-translate-y-1 transition-all duration-300 flex flex-col items-center text-center"
      >
        <div
          class="flex items-center justify-center w-16 h-16 rounded-2xl bg-gradient-to-br from-gray-900 to-gray-700 text-white shadow-md group-hover:scale-110 transition-transform duration-300"
        >
          <svelte:component this={service.icon} size="36" />
        </div>
        <h3 class="mt-5 text-xl font-semibold text-gray-900">
          {service.title}
        </h3>
        <p class="mt-3 text-gray-600 leading-relaxed">
          {service.desc}
        </p>
      </div>
    {/each}
  </section>

  <!-- FEATURE SECTION -->
  <section class="flex flex-col md:flex-row items-center gap-14">
    <div class="md:w-1/2 space-y-6">
      <h2
        class="text-3xl md:text-4xl font-bold text-gray-900 font-['Playfair_Display']"
      >
        Why Choose Iconic Kennels
      </h2>
      <p class="text-gray-600 leading-relaxed">
        With a heritage rooted in care, science, and trust, Iconic Kennels
        produces dogs of superior health, temperament, and beauty — companions
        for life.
      </p>
      <ul class="text-gray-700 list-disc list-inside space-y-2">
        <li>Ethical, health-first breeding practices.</li>
        <li>Personalized training aligned with lifestyle goals.</li>
        <li>Ongoing lifetime support for every family.</li>
      </ul>
      <button
        class="mt-6 px-8 py-3 bg-gradient-to-r from-gray-900 to-gray-700 text-white font-semibold rounded-full shadow hover:opacity-90 transition"
      >
        Contact Us
      </button>
    </div>

    <div class="md:w-1/2 flex flex-col md:flex-row gap-6 relative">
      <img
        src={dog1}
        alt="German Shepherd 1"
        class="rounded-3xl w-full md:w-2/3 h-[360px] object-cover shadow-xl"
      />
      <div class="flex flex-col gap-6 w-full md:w-1/3">
        <img
          src={dog2}
          alt="German Shepherd 2"
          class="rounded-3xl h-[170px] object-cover shadow-md"
        />
        <img
          src={dog3}
          alt="German Shepherd 3"
          class="rounded-3xl h-[170px] object-cover shadow-md"
        />
      </div>
      <div
        class="absolute inset-0 bg-gradient-to-r from-white/5 to-transparent rounded-3xl pointer-events-none"
      ></div>
    </div>
  </section>

  <!-- CTA SECTION -->
  <section class="relative text-center rounded-3xl overflow-hidden py-20 px-8">
    <div
      class="absolute inset-0 bg-gradient-to-br from-gray-900 via-gray-800 to-gray-700"
    ></div>
    <div class="relative z-10 space-y-6 text-white">
      <h2 class="text-3xl md:text-4xl font-bold font-['Playfair_Display']">
        Ready to Begin Your Journey?
      </h2>
      <p class="text-gray-300 max-w-xl mx-auto leading-relaxed">
        Whether you're adopting, training, or boarding, we’ll walk every step
        with you — raising companions who are truly iconic.
      </p>
      <button
        class="px-10 py-3 bg-white text-black font-semibold rounded-full hover:bg-gray-100 transition"
      >
        Get in Touch
      </button>
    </div>
  </section>
</div>
