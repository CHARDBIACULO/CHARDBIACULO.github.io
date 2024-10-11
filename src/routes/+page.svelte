<script>
// @ts-nocheck

  import Button from '../components/showcontact.svelte';
  import Navbar from '../components/navbar.svelte';
  import Profile from '../components/Profile.svelte'; // Adjust the path as necessary
  import Footer from '../components/footer.svelte';
</script>

<main class="mt-8 bg-cover bg-center min-h-screen text-white relative" style="background-image: url('/path-to-your-background-image.jpg');">
  <!-- Overlay -->
  <div class="absolute inset-0 bg-transparent opacity-70"></div>

  <!-- Content Wrapper -->
  <div class="relative z-10">
    <Navbar />
    <Profile />

    <!-- Hero Section -->
    <section id="home" class="py-20 md:py-28 text-center">
      <div class="container mx-auto px-6">
        <h1 class="text-5xl md:text-7xl font-bold text-white mb-6 leading-tight">
          Hi, I'm <span class="text-yellow-300">Richard Angelo T. Biaculo Supot at si Nandy</span>
        </h1>
        <h2 class="text-2xl md:text-3xl font-semibold text-gray-200 mb-6">
          Third Year Computer Science Student at Gordon College
        </h2>
        <p class="text-lg md:text-xl text-gray-300 max-w-xl mx-auto">
          Passionate about web development and dedicated to building impactful projects.
        </p>
      </div>
    </section>

    <!-- Introduction Section -->
    <section id="about" class="py-20 md:py-28 bg-transparent bg-opacity-80 rounded-lg shadow-lg">
      <div class="container mx-auto px-6 text-center">
        <h3 class="text-4xl md:text-5xl font-bold text-white mb-6">
          Welcome to My <span class="text-yellow-300">Professional Portfolio</span>
        </h3>
        <p class="text-lg md:text-xl text-gray-300 max-w-2xl mx-auto">
          Explore my projects, learn about my journey, and feel free to connect for collaboration.
        </p>
      </div>
    </section>

    <!-- Call to Action Section -->
    <section id="scroll-info" class="py-20 md:py-28 bg-transparent bg-opacity-90 rounded-lg shadow-lg">
      <div class="container mx-auto px-6 text-center">
        <h3 class="text-4xl md:text-5xl font-bold text-yellow-300 mb-4">
          Explore My Work
        </h3>
        <p class="text-lg md:text-xl text-gray-300 mb-8">
          Learn more about my journey, and get in touch for potential collaborations.
        </p>
        <div class="flex justify-center">
          <Button class="bg-purple-600 text-white px-8 py-4 rounded-lg shadow-lg hover:bg-purple-700 transition-all duration-300" />
        </div>
      </div>
    </section>

    <Footer />
  </div>
</main>

<style>
:global(body) {
  scroll-behavior: smooth;
  font-family: 'Roboto', sans-serif;
  margin: 0;
  padding: 0;
}

main {
  animation: fadeIn 1s ease-in-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

/* Ensure background image covers the entire viewport */
.bg-cover {
  background-size: cover;
  background-repeat: no-repeat;
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .text-5xl {
    font-size: 3rem;
  }
}
</style>
