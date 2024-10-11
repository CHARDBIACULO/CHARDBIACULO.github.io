<script>
  import { Carousel } from 'flowbite-svelte';
  import { scale } from 'svelte/transition';
  import { quintOut } from 'svelte/easing';

  const scaleAnimation = (x) => scale(x, { duration: 500, easing: quintOut });

  const images = [
    {
      alt: 'First Weather Image',
      src: 'images/kanban1.jpg',
      title: 'Explore Different Weathers'
    },
    {
      alt: 'Profile Image 1',
      src: 'images/kanban2.jpg',
      title: 'User Profile Overview'
    },
    {
      alt: 'Profile Image 2',
      src: 'images/kanban3.jpg',
      title: 'User Profile Insights'
    },
  ];
</script>
  <!-- Center the carousel horizontally -->
  <div class="max-w-4xl mx-auto">
    <Carousel {images} transition={scaleAnimation} let:Controls let:Indicators>
      <Controls />
      <Indicators />
    </Carousel>
  </div>
  