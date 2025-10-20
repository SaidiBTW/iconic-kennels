<script lang="ts">
  let form = {
    fullName: "",
    address: "",
    email: "",
    phone: "",
    dogDetails: "",
    breedingExperience: "",
  };

  const handleSubmit = (event: Event) => {
    event.preventDefault();
    console.log("Stud form submitted:", form);
    alert("Your stud application has been successfully submitted!");
  };
</script>

<section class="max-w-3xl mx-auto px-6 py-12">
  <!-- Header -->
  <div class="text-center mb-10">
    <h1 class="text-4xl font-bold font-['Playfair_Display'] mb-3">
      German Shepherd Stud Application
    </h1>
    <p class="text-gray-600 max-w-2xl mx-auto">
      If you own a German Shepherd male and would like to register him for stud
      services, please fill out the form below. Our team will review your
      application and get back to you.
    </p>
  </div>

  <!-- Form Card -->
  <form
    on:submit|preventDefault={handleSubmit}
    class="bg-white shadow-md rounded-2xl p-8 space-y-6 border border-gray-100"
  >
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
      <div>
        <label for="fullName" class="block text-sm font-semibold mb-1"
          >Full Name</label
        >
        <input
          id="fullName"
          type="text"
          bind:value={form.fullName}
          placeholder="Enter your full name"
          class="w-full border border-gray-300 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 rounded-lg px-3 py-2 transition"
          required
        />
      </div>

      <div>
        <label for="email" class="block text-sm font-semibold mb-1">Email</label
        >
        <input
          id="email"
          type="email"
          bind:value={form.email}
          placeholder="you@example.com"
          class="w-full border border-gray-300 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 rounded-lg px-3 py-2 transition"
          required
        />
      </div>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
      <div>
        <label for="phone" class="block text-sm font-semibold mb-1"
          >Phone Number</label
        >
        <input
          id="phone"
          type="tel"
          bind:value={form.phone}
          placeholder="(123) 456-7890"
          class="w-full border border-gray-300 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 rounded-lg px-3 py-2 transition"
          required
        />
      </div>

      <div>
        <label for="address" class="block text-sm font-semibold mb-1"
          >Address</label
        >
        <input
          id="address"
          type="text"
          bind:value={form.address}
          placeholder="Your current address"
          class="w-full border border-gray-300 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 rounded-lg px-3 py-2 transition"
          required
        />
      </div>
    </div>

    <div>
      <label for="dogDetails" class="block text-sm font-semibold mb-1">
        Dog Details (Name, Age, Health Status)
      </label>
      <textarea
        id="dogDetails"
        bind:value={form.dogDetails}
        placeholder="E.g. Rex, 4 years old, healthy with vaccination records up to date."
        rows="3"
        class="w-full border border-gray-300 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 rounded-lg px-3 py-2 transition resize-none"
        required
      ></textarea>
    </div>

    <div>
      <label for="breedingExperience" class="block text-sm font-semibold mb-1">
        Breeding Experience
      </label>
      <textarea
        id="breedingExperience"
        bind:value={form.breedingExperience}
        placeholder="Describe your experience with breeding and past litters, if any."
        rows="4"
        class="w-full border border-gray-300 focus:border-blue-500 focus:ring-2 focus:ring-blue-100 rounded-lg px-3 py-2 transition resize-none"
        required
      ></textarea>
    </div>

    <div class="pt-4 text-center">
      <button
        type="submit"
        class="bg-blue-600 text-white font-semibold px-6 py-3 rounded-lg hover:bg-blue-700 transition shadow-sm"
      >
        Submit Application
      </button>
    </div>
  </form>
</section>
