<script lang="ts">
  import dog1 from "$lib/assets/dog1.jpeg";
  import dog2 from "$lib/assets/dog2.jpeg";
  import dog3 from "$lib/assets/dog3.jpeg";
  import dog4 from "$lib/assets/dog4.jpeg";

  const testimonials = [
    {
      src: dog1,
      dog_name: "Buddy",
      name: "John Doe",
      feedback: "Great service!",
    },
    {
      src: dog2,
      dog_name: "Max",
      name: "Jane Smith",
      feedback: "My dog loves it here!",
    },
    {
      src: dog3,
      dog_name: "Charlie",
      name: "Bob Johnson",
      feedback: "Highly recommend!",
    },
    {
      src: dog4,
      dog_name: "Bella",
      name: "Miley Cyrus",
      feedback: "Fantastic experience!",
    },
  ];
</script>

<div class="flex overflow-x-auto snap-x snap-mandatory scroll-smooth">
  {#each testimonials as item}
    <div
      class="flex-shrink-0 w-full sm:w-1/2 md:w-full p-2 flex items-center justify-center snap-center"
    >
      <!--Circle Avatar-->
      <div
        class="w-48 h-48 rounded-full overflow-hidden border-4 border-blue-500"
      >
        <img
          src={item.src}
          alt={item.dog_name}
          class="object-cover w-full h-full"
        />
      </div>

      <!--Text Column-->
      <div class="flex flex-col ml-6 text-center">
        <h3>
          "{item.dog_name}": {item.feedback}
        </h3>
        <h1 class="text-2xl font-bold mt-2">
          "{item.name}"
        </h1>
      </div>
    </div>
  {/each}
</div>
