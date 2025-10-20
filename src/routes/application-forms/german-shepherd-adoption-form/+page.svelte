<script lang="ts">
  let fullName: string = "";
  let address: string = "";
  let email: string = "";
  let phone: string = "";
  let reasonForAdoption: string = "";
</script>

<h1 class="text-3xl font-bold mb-4">German Shepherd Adoption Form</h1>
<form class="space-y-4">
  <div>
    <label for="fullName" class="block text-lg font-medium mb-1"
      >Full Name:</label
    >
    <input
      id="fullName"
      type="text"
      bind:value={fullName}
      class="w-full border border-gray-300 rounded px-3 py-2"
      required
    />
  </div>
  <div>
    <label for="address" class="block text-lg font-medium mb-1">Address:</label>
    <input
      id="address"
      type="text"
      bind:value={address}
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
    <label for="reasonForAdoption" class="block text-lg font-medium mb-1"
      >Reason for Adoption:</label
    >
    <textarea
      id="reasonForAdoption"
      bind:value={reasonForAdoption}
      class="w-full border border-gray-300 rounded px-3 py-2"
      rows="4"
      required
    ></textarea>
  </div>
  <button
    type="submit"
    class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700"
  >
    Submit Application
  </button>
</form>
