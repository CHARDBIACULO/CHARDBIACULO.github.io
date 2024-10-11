<script>
  import    Navbar            from '../../components/navbar.svelte';
  import    Footer            from '../../components/footer.svelte';
  import    Carousel1          from '../../components/carousel1.svelte';
  import    Carousel2          from '../../components/carousel2.svelte';
  import    Carousel3          from '../../components/carousel3.svelte';
  
  import { Progressbar }      from 'flowbite-svelte';
</script>

<main>
<Navbar />

<section class="py-16">
  <div class="text-center">
    <h1 class="text-5xl font-bold mb-4 text-yellow-300">Welcome to My Portfolio</h1>
    <p class="text-xl ">Here you will find information my projects.</p>
  </div>
</section>

<section class="py-16">
  <div class="text-center">
  <h2 class="text-5xl font-bold mb-4 text-yellow-300">Kanban(drag and drop)<h2>
  <p class="text-2xl text-white">(ANGULAR)</p>
  <Carousel1 />
  <div class="mb-1 text-base font-medium  dark:text-purple-400">Progress 100%</div>
  <div class="max-w-4xl mx-auto">
    <Progressbar progress="100" color="yellow" />
  </div>
 </div>
</section>

<section class="py-16">
  <div class="text-center">
  <h3 class="text-5xl font-bold mb-4 text-yellow-300">To Do list</h3>
  <p class="text-2xl text-white">(PHP)</p>
  <Carousel2 />
   <div class="mb-1 text-base font-medium dark:text-purple-400">Progress 100%</div>
    <div class="max-w-4xl mx-auto">
      <Progressbar progress="100" color="yellow" />
    </div>
   </div>
</section>

<section class="py-16">
  <div class="text-center">
  <h4 class="text-5xl font-bold mb-4 text-yellow-300">Advance Calculator</h4>
  <p class="text-2xl text-white">(JAVA)</p>
  <Carousel3 />
  <div class="mb-1 text-base font-medium  dark:text-purple-400">Progress 50%</div>
  <div class="max-w-4xl mx-auto">
    <Progressbar progress="50" color="yellow" />
  </div>
 </div>
</section>

=

<Footer />
</main>

<style>
main {
  margin: 0;
  padding: 0;
}
</style>
