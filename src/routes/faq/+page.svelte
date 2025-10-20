<script lang="ts">
  interface FAQ {
    question: string;
    answer: string;
    open?: boolean;
  }

  let faqs: FAQ[] = [
    {
      question: "What services do you offer?",
      answer:
        "We specialize in German Shepherd breeding, adoption services, and provide expert training advice to help new owners raise well-behaved companions.",
    },
    {
      question: "How can I adopt a German Shepherd?",
      answer:
        "Visit our Application Forms page to complete the adoption form. Our team will review your application and contact you to discuss the next steps.",
    },
    {
      question: "Do you provide training for German Shepherds?",
      answer:
        "Yes, we offer basic obedience guidance and connect you with professional trainers to ensure your German Shepherd gets the best start.",
    },
  ];

  const toggle = (index: number) => {
    faqs = faqs.map((faq, i) =>
      i === index ? { ...faq, open: !faq.open } : { ...faq, open: false }
    );
  };
</script>

<section class="max-w-4xl mx-auto px-4 py-12">
  <h1 class="text-4xl font-bold text-center text-gray-900 mb-10">
    Frequently Asked Questions
  </h1>

  <div class="space-y-4">
    {#each faqs as faq, i}
      <div
        class="border border-gray-200 rounded-xl shadow-sm bg-white transition hover:shadow-md"
      >
        <button
          on:click={() => toggle(i)}
          class="w-full flex justify-between items-center px-6 py-4 text-left focus:outline-none"
        >
          <span class="text-lg font-medium text-gray-800">{faq.question}</span>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="2"
            stroke="currentColor"
            class="w-5 h-5 text-gray-600 transition-transform duration-300"
            class:rotate-180={faq.open}
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M19 9l-7 7-7-7"
            />
          </svg>
        </button>

        <div
          class="overflow-hidden transition-all duration-300"
          style="max-height: {faq.open ? '200px' : '0'}"
        >
          <div class="px-6 pb-4 text-gray-600 leading-relaxed">
            {faq.answer}
          </div>
        </div>
      </div>
    {/each}
  </div>
</section>
