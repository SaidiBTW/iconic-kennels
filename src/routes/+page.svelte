<script>
  import dog1 from "$lib/assets/dog1.jpeg";
  import dog2 from "$lib/assets/dog2.jpeg";
  import dog3 from "$lib/assets/dog3.jpeg";
  import { FacebookIcon, InstagramIcon, PawPrint } from "@lucide/svelte";
</script>

<div class="max-w-screen">
  <div>
    <h1 class="text-3xl font-bold mb-4">Welcome to Iconic Kennels</h1>
    <p class="mb-4">
      We are delighted to have you here! At Iconic Kennels, we are passionate
      about providing the best care and services for your beloved pets. Whether
      you're looking to adopt a new furry friend, need top-notch grooming, or
      require reliable boarding services, we've got you covered.
    </p>
    <p class="mb-4">
      Explore our website to learn more about our services, meet our adorable
      dogs available for adoption, and find answers to frequently asked
      questions. If you have any inquiries or would like to get in touch with
      us, please don't hesitate to visit our Contact page.
    </p>
    <p>
      Thank you for choosing Iconic Kennels – where every pet is treated like
      family!
    </p>
  </div>

  <div class="grid grid-cols-3 gap-4 mt-8 md:grid place-items-center">
    <div class="bg-gray-100 p-4 rounded">
      <PawPrint size="48" color="#4A5568" />
      <p class="mt-2 text-center font-semibold">Dog 1</p>
      <button
        class="mt-2 px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700"
      >
        Learn More
      </button>
    </div>
    <div class="bg-gray-100 p-4 rounded">
      <PawPrint size="48" color="#4A5568" />
      <p class="mt-2 text-center font-semibold">Dog 2</p>
      <button
        class="mt-2 px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700"
      >
        Learn More
      </button>
    </div>
    <div class="bg-gray-100 p-4 rounded flex-col justify-center">
      <PawPrint class="mt-2 ce" size="48" color="#4A5568" />
      <p class="mt-2 text-center font-semibold">Photo Gallery</p>
      <button
        class="mt-2 px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700"
      >
        View Gallery
      </button>
    </div>
  </div>
</div>

<br />
<!-- Meet the Champions of Iconic Kennels -->

<div>
  <div class="flex justify-items-center items-center">
    <h2 class="text-2xl font-bold mb-4">
      Meet the Champions of Iconic Kennels
    </h2>
    <div class="bg-gray-100 p-4 rounded">
      <p>
        At Iconic Kennels, we take immense pride in our German Shepherds who
        have not only won hearts but also prestigious titles in various
        competitions. Our champions are a testament to our dedication to
        breeding excellence and superior care.
      </p>
      <p class="mt-4">
        Each of our champion German Shepherds has undergone rigorous training
        and has been recognized for their outstanding qualities, including
        obedience, agility, and temperament. They serve as role models for our
        breeding program, ensuring that we continue to produce top-tier dogs for
        our clients.
      </p>
    </div>
  </div>
  <div class="flex grid-cols-3 gap-4 mt-8 md:grid place-items-center">
    <div class="bg-gray-100 p-4 rounded">
      <img
        src={dog1}
        alt="Champion 1"
        class="mb-2 rounded w-60 h-60 object-cover"
      />
      <p class="mt-2 text-center font-semibold">Champion 1</p>
      <button
        class="mt-2 px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700"
      >
        Learn More
      </button>
    </div>
    <div class="bg-gray-100 p-4 rounded">
      <img
        src={dog2}
        alt="Champion 2"
        class="mb-2 rounded w-60 h-60 object-cover"
      />
      <p class="mt-2 text-center font-semibold">Champion 2</p>
      <button
        class="mt-2 px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700"
      >
        Learn More
      </button>
    </div>
    <div class="bg-gray-100 p-4 rounded">
      <img
        src={dog3}
        alt="Champion 3"
        class="mb-2 rounded w-60 h-60 object-cover"
      />
      <p class="mt-2 text-center font-semibold">Champion 3</p>
      <button
        class="mt-2 px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700"
      >
        Learn More
      </button>
    </div>
  </div>
  <!-- <Carousel /> -->
  <div class="mt-8">
    <h2 class="text-2xl font-bold mb-4">What Our Clients Say</h2>
    <p>
      Don't just take our word for it – hear what our satisfied clients have to
      say about their experiences with Iconic Kennels. Our commitment to
      excellence and genuine care for every pet has earned us glowing reviews
      and heartfelt testimonials.
    </p>
  </div>

  <div class="grid-cols-2 gap-4 mt-8 md:grid place-items-center">
    <div class="bg-gray-100 p-4 rounded">
      <p class="italic">
        "Iconic Kennels provided exceptional care for my German Shepherd while I
        was away. The staff was friendly, and I could tell my dog was in good
        hands. Highly recommend!"
      </p>
      <p class="mt-2 font-semibold text-right">- Sarah L.</p>
    </div>
    <div class="bg-gray-100 p-4 rounded">
      <p class="italic">
        "The adoption process at Iconic Kennels was smooth and enjoyable. I
        found the perfect companion, and the team was supportive every step of
        the way."
      </p>
      <p class="mt-2 font-semibold text-right">- Mark D.</p>
    </div>
  </div>

  <div class="grid-cols-2 gap-4">
    <div class="bg-gray-100 p-4 rounded mt-4">
      <p class="italic">
        "I can't thank Iconic Kennels enough for their grooming services. My dog
        looks fantastic and feels great after every visit!"
      </p>
      <p class="mt-2 font-semibold text-right">- Emily R.</p>
    </div>
    <div class="bg-gray-100 p-4 rounded mt-4">
      <p class="italic">
        "From the moment I walked into Iconic Kennels, I felt welcomed. Their
        passion for dogs is evident, and they truly care about the well-being of
        each pet."
      </p>
      <p class="mt-2 font-semibold text-right">- James K.</p>
    </div>
  </div>
  <h2 class="text-2xl font-bold mt-8">Connect with Us</h2>
  <div class="flex mt-8 space-x-4">
    <a
      href="https://www.facebook.com/iconickennels"
      target="_blank"
      rel="noopener noreferrer"
      class="text-blue-600 hover:text-blue-800"
    >
      <FacebookIcon size="32" />
    </a>
    <a
      href="https://www.instagram.com/iconickennels"
      target="_blank"
      rel="noopener noreferrer"
      class="text-pink-600 hover:text-pink-800"
    >
      <InstagramIcon size="32" />
    </a>
  </div>
</div>
