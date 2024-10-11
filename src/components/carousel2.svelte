<script>
    import { Carousel } from 'flowbite-svelte';
    import { scale } from 'svelte/transition';
    import { quintOut } from 'svelte/easing';
  
    const scaleAnimation = (x) => scale(x, { duration: 500, easing: quintOut });
  
    // Define your own images array here
    const images = [
      {
        alt: 'My First Image',
        src: 'images/todo1.jpg',
        title: 'Image 1 Description'
      },
     
      // Add more images as needed
    ];
  </script>
  
  <!-- Center the carousel horizontally -->
  <div class="max-w-4xl mx-auto">
    <Carousel {images} transition={scaleAnimation} let:Controls let:Indicators>
      <Controls />
      <Indicators />
    </Carousel>
  </div>
  