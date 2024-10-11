<script>
  import Navbar from '../../components/navbar.svelte';
  import Footer from '../../components/footer.svelte';
  import Carousel4 from '../../components/carousel4.svelte';

</script>

<main class="bg-transparent">
  <Navbar />
  
  <!-- About Me Section -->
  <section id="about" class="py-16 bg-transparent shadow-lg rounded-lg mb-8">
    <div class="container mx-auto px-6">
      <h1 class="text-5xl font-bold text-white-700 mb-6 text-center">About Me</h1>
      <h2 class="text-2xl font-medium text-white-600 mb-6 text-center">
        Hi! Im Richard Angelo T. Biaculo you can call me chard inshort, a dedicated third-year Computer Science student at Gordon College, aspiring to become a front-end developer.
      </h2>
      <div class="flex flex-col md:flex-row items-center">
        <!-- About Me Content -->
        <div class="md:w-2/3 mb-8 md:mb-0">
          <p class="text-lg text-gray-700 mb-4">
            Currently, I work as a freelancer in non-IT fields, taking on roles such as Waiter, Caterer, and Lights and Sounds Helper.
          </p>     
          <p class="text-lg text-gray-700 mb-4">
          I also love playing game, do a roadtrip with my GF and  Frinds, but also pursuing to be a successful man to give my family the dream they have and also to give back the love they give to me.
          </p>
        </div>
      </div>
    </div>    
  </section>

  <!-- Journey Section -->
  <section id="journey" class="py-16 bg-transparent shadow-lg rounded-lg">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl text-white-700 font-bold mb-6">My Journey as a Student Developer</h2>
      <p class="mb-4 text-gray-700">
        As a third-year Computer Science student at Gordon College, my journey in technology has been both challenging and fulfilling. I've explored a wide range of topics, from foundational programming concepts to specialized areas like web development and machine learning.
        My coursework has provided me with a strong understanding of algorithms, data structures, and software engineering principles. I’ve applied this knowledge through various projects, including a blog application built with Angular and PHP, which honed my skills in full-stack development and user authentication.
        Beyond the classroom, I’ve gained practical experience through freelance work and personal projects. These opportunities have sharpened my front-end development skills, strengthened my problem-solving abilities, and improved my time management. I take pride in building responsive, user-friendly interfaces and have recently enjoyed diving into newer technologies like Svelte.
        As I look to the future, I’m excited to continue my growth toward becoming a front-end developer. I’m eager to embrace new challenges, collaborate on innovative projects, and further refine my ability to create dynamic and engaging web experiences.
      </p>
    </div>
    <Carousel4 />
  </section>
  <Footer />
  
</main>


<style>
  main {
    margin-top: 2rem;
    font-family: 'Arial', sans-serif;
  }

  h1, h2 {
    text-align: center;
  }
</style>


