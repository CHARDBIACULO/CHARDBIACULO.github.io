<script>
    import { Carousel } from 'flowbite-svelte';
    import { scale } from 'svelte/transition';
    import { quintOut } from 'svelte/easing';
  
    const scaleAnimation = (x) => scale(x, { duration: 500, easing: quintOut });
  
    // Define your own images array here
    const images = [
      {
        alt: 'My First Image',
        src: 'images/cater1.jpg',
        title: 'Image 1 Description'
      },
      {
        alt: 'My First Image',
        src: 'images/cater2.jpg',
        title: 'Image 1 Description'
      },
      {
        alt: 'My First Image',
        src: 'images/cater3.jpg',
        title: 'Image 1 Description'
      },
      {
        alt: 'My First Image',
        src: 'images/cater4.jpg',
        title: 'Image 1 Description'
      },
      {
        alt: 'My First Image',
        src: 'images/cater5.jpg',
        title: 'Image 1 Description'
      },
      {
        alt: 'My First Image',
        src: 'images/cater6.jpg',
        title: 'Image 1 Description'
      },
      {
        alt: 'My First Image',
        src: 'images/cater7.jpg',
        title: 'Image 1 Description'
      },
     
      // Add more images as needed
    ];
  </script>
  
<!-- Carousel container -->
<div class="flex items-center justify-center w-full h-screen">
  <div class="max-w-4xl w-full space-y-4">
  <h1 class="text-5xl font-bold mb-4 text-yellow-400 text-center">My Album</h1>
    <Carousel {images} imgClass="object-contain h-full w-fit rounded-sm" let:Indicators let:Controls class="rounded-md ring-4 ring-yellow-500 border-4 border-white dark:border-gray-800 min-h-[320px] bg-transparent">
      <Indicators class="border border-white rounded-md p-2" />
      <Controls class="items-center text-red-400 dark:text-black-400 pt-4" />
    </Carousel>
  </div>
</div>  
  