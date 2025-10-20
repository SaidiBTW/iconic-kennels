<!--The FAQ page is designed to answer common questions about our services and German Shepherd care. -->

<script lang="ts">
  import { onMount } from "svelte";

  interface FAQ {
    question: string;
    answer: string;
  }

  let faqs: FAQ[] = [];

  onMount(() => {
    // Fetch FAQ data or define it here
    faqs = [
      {
        question: "What services do you offer?",
        answer:
          "We offer German Shepherd breeding, adoption services, and training advice.",
      },
      {
        question: "How can I adopt a German Shepherd?",
        answer:
          "You can visit our Application Forms page to fill out the adoption application.",
      },
      {
        question: "Do you provide training for German Shepherds?",
        answer:
          "Yes, we offer basic training tips and resources for new owners.",
      },
    ];
  });
</script>

<h1 class="text-3xl font-bold mb-4">Frequently Asked Questions</h1>
{#each faqs as faq}
  <div class="mb-6">
    <h2 class="text-2xl font-semibold mb-2">{faq.question}</h2>
    <p class="text-gray-700">{faq.answer}</p>
  </div>
{/each}
