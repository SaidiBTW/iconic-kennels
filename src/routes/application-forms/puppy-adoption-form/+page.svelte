<!--
  This is the puppy adoption form page where users can fill out the necessary information to adopt a puppy.
  The form will include fields for the user's name, contact information, and details about the puppy they wish to adopt.
   -- Email
   -- Phone Number
    -- Puppy Preference (if any)
  The form will also include a submit button to send the application.
-->

<script lang="ts">
  let name: string = "";
  let email: string = "";
  let phone: string = "";
  let puppyPreference: string = "";
</script>

<h1 class="text-3xl font-bold mb-4">Puppy Adoption Form</h1>
<form class="space-y-4">
  <div>
    <label for="name" class="block text-lg font-medium mb-1">Name:</label>
    <input
      id="name"
      type="text"
      bind:value={name}
      class="w-full border border-gray-300 rounded px-3 py-2"
      required
    />
  </div>
  <div>
    <label for="email" class="block text-lg font-medium mb-1">Email:</label>
    <input
      id="email"
      type="email"
      bind:value={email}
      class="w-full border border-gray-300 rounded px-3 py-2"
      required
    />
  </div>
  <div>
    <label for="phone" class="block text-lg font-medium mb-1"
      >Phone Number:</label
    >
    <input
      id="phone"
      type="tel"
      bind:value={phone}
      class="w-full border border-gray-300 rounded px-3 py-2"
      required
    />
  </div>
  <div>
    <label for="puppyPreference" class="block text-lg font-medium mb-1"
      >Puppy Preference (if any):</label
    >
    <input
      id="puppyPreference"
      type="text"
      bind:value={puppyPreference}
      class="w-full border border-gray-300 rounded px-3 py-2"
    />
  </div>
  <button
    type="submit"
    class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600"
  >
    Submit Application
  </button>
</form>
