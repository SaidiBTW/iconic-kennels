<script lang="ts">
  import dog1 from "$lib/assets/dog1.jpeg";
  import {
    FacebookIcon,
    GalleryVertical,
    InstagramIcon,
    PawPrint,
  } from "@lucide/svelte";

  function handleViewGallery() {
    window.location.href = "/gallery";
  }
</script>

<!-- Hero Section -->
<section class="max-w-6xl mx-auto px-6 py-12">
  <div class="text-center mb-12">
    <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">
      Welcome to Iconic Kennels
    </h1>
    <p class="text-gray-600 max-w-3xl mx-auto leading-relaxed">
      At Iconic Kennels, we’re passionate about raising exceptional German
      Shepherds with care, ethics, and love. Whether you're looking to adopt,
      train, or learn more about our champions, you’re in the right place.
    </p>
  </div>

  <!-- Intro Cards -->
  <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
    <div
      class="bg-white shadow-sm hover:shadow-md transition-all p-8 rounded-2xl flex flex-col items-center text-center"
    >
      <PawPrint size="56" color="#1f2937" />
      <h3 class="mt-4 text-xl font-semibold text-gray-800">Planned Litters</h3>
      <p class="mt-2 text-gray-600 text-sm">
        Explore our upcoming litters from award-winning bloodlines.
      </p>
      <button
        class="mt-4 px-5 py-2 bg-black text-white rounded-lg hover:bg-gray-800 transition-colors"
      >
        Learn More
      </button>
    </div>

    <div
      class="bg-white shadow-sm hover:shadow-md transition-all p-8 rounded-2xl flex flex-col items-center text-center"
    >
      <GalleryVertical size="56" color="#1f2937" />
      <h3 class="mt-4 text-xl font-semibold text-gray-800">Photo Gallery</h3>
      <p class="mt-2 text-gray-600 text-sm">
        Browse through our gallery of champions and proud owners.
      </p>
      <button
        class="mt-4 px-5 py-2 bg-black text-white rounded-lg hover:bg-gray-800 transition-colors"
        onclick={handleViewGallery}
      >
        View Gallery
      </button>
    </div>
  </div>
</section>

<!-- Champions Section -->
<section class="bg-gray-50 py-16 px-6">
  <div class="max-w-6xl mx-auto flex flex-col md:flex-row items-center gap-10">
    <div class="md:w-1/2">
      <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-6">
        Meet the Champions of Iconic Kennels
      </h2>
      <p class="text-gray-700 leading-relaxed">
        Our German Shepherds are a testament to quality, discipline, and
        heritage. Each champion has been raised with care and recognized for
        excellence in obedience, agility, and temperament.
      </p>
      <p class="mt-4 text-gray-700 leading-relaxed">
        These champions form the foundation of our breeding program — ensuring
        every puppy inherits the same legacy of excellence.
      </p>
    </div>

    <div class="md:w-1/2 flex justify-center">
      <img
        src={dog1}
        alt="Champion Dogs"
        class="rounded-2xl shadow-md object-cover w-full max-h-[400px]"
      />
    </div>
  </div>

  <!-- Champion Cards -->
  <div
    class="mt-16 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 place-items-center"
  >
    {#each Array(3) as _, i}
      <div
        class="bg-white p-6 rounded-2xl shadow-sm hover:shadow-lg transition-shadow duration-300 flex flex-col items-center w-full max-w-sm"
      >
        <img
          src={dog1}
          alt="Champion {i + 1}"
          class="rounded-xl w-full h-60 object-cover mb-4"
        />
        <h3 class="text-xl font-bold text-gray-900 text-center">
          Champion Zeus von Iconic
        </h3>
        <p class="text-sm text-gray-500 text-center mb-3">
          German Shepherd • 3x National Winner
        </p>
        <div class="flex justify-around w-full text-sm text-gray-600 mb-4">
          <div class="text-center">
            <p class="font-semibold text-gray-800">4</p>
            <p>Titles</p>
          </div>
          <div class="text-center">
            <p class="font-semibold text-gray-800">5 yrs</p>
            <p>Age</p>
          </div>
          <div class="text-center">
            <p class="font-semibold text-gray-800">Kenya</p>
            <p>Origin</p>
          </div>
        </div>
        <button
          class="mt-auto px-6 py-2 bg-black text-white font-medium rounded-lg hover:bg-gray-800 transition-colors"
        >
          Learn More
        </button>
      </div>
    {/each}
  </div>
</section>

<!-- Testimonials -->
<section class="max-w-6xl mx-auto py-16 px-6">
  <h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-10 text-center">
    What Our Clients Say
  </h2>
  <div class="grid md:grid-cols-2 gap-8">
    <div
      class="bg-white p-6 rounded-2xl shadow-sm hover:shadow-md transition-shadow"
    >
      <p class="italic text-gray-700">
        “Iconic Kennels provided exceptional care for my German Shepherd while I
        was away. The staff was friendly, and I could tell my dog was in good
        hands. Highly recommend!”
      </p>
      <p class="mt-4 font-semibold text-right text-gray-900">- Sarah L.</p>
    </div>
    <div
      class="bg-white p-6 rounded-2xl shadow-sm hover:shadow-md transition-shadow"
    >
      <p class="italic text-gray-700">
        “The adoption process at Iconic Kennels was smooth and enjoyable. I
        found the perfect companion, and the team was supportive every step of
        the way.”
      </p>
      <p class="mt-4 font-semibold text-right text-gray-900">- Mark D.</p>
    </div>
    <div
      class="bg-white p-6 rounded-2xl shadow-sm hover:shadow-md transition-shadow"
    >
      <p class="italic text-gray-700">
        “Their grooming services are unmatched. My dog looks fantastic and feels
        great after every visit!”
      </p>
      <p class="mt-4 font-semibold text-right text-gray-900">- Emily R.</p>
    </div>
    <div
      class="bg-white p-6 rounded-2xl shadow-sm hover:shadow-md transition-shadow"
    >
      <p class="italic text-gray-700">
        “From the moment I walked in, I felt welcomed. Their passion for dogs is
        evident — they truly care about each pet.”
      </p>
      <p class="mt-4 font-semibold text-right text-gray-900">- James K.</p>
    </div>
  </div>
</section>

<!-- Social Section -->
<section class="bg-gray-50 py-12">
  <div class="max-w-6xl mx-auto text-center">
    <h2 class="text-3xl font-bold text-gray-900 mb-6">Connect with Us</h2>
    <div class="flex justify-center space-x-6">
      <a
        href="https://www.facebook.com/iconickennels"
        target="_blank"
        class="text-blue-600 hover:text-blue-800 transition-colors"
      >
        <FacebookIcon size="36" />
      </a>
      <a
        href="https://www.instagram.com/iconickennels"
        target="_blank"
        class="text-pink-600 hover:text-pink-800 transition-colors"
      >
        <InstagramIcon size="36" />
      </a>
    </div>
  </div>
</section>
