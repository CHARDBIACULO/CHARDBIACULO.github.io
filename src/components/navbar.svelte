<!-- This is a NavBar with ButtonGroup -->
<!-- I made this with the help of Chatgpt and flowbite -->

<script>
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
  import { ButtonGroup, Button } from 'flowbite-svelte';
  import { onMount } from 'svelte';

  let navbarVisible = true; // State variable to track visibility of navbar

  // Function to set up the intersection observer
  function setupObserver() {
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          navbarVisible = entry.isIntersecting; // Update the state based on intersection
        });
      },
      {
        root: null, // Use the viewport as the root
        threshold: 0, // Trigger when even a pixel is visible
      }
    );

    // Observe the navbar element
    const navbarElement = document.querySelector('#navbar');
    if (navbarElement) {
      observer.observe(navbarElement);
    }
  }

  // Run the observer setup on component mount
  onMount(() => {
    setupObserver();
  });
</script>

<style>
  .hidden {
    display: none;
  }
</style>

<!-- Navbar -->
<Navbar class="container mx-auto p-4 bg-transparent">
  <!-- NavBrand: Circular image with bigger size -->
  <NavBrand href="https://www.facebook.com/richard.biaculo" class="flex items-center space-x-4">
    <img src="images/profile.png" alt="Profile pic" class="h-20 w-20 rounded-full sm:h-20 sm:w-20">
    <!-- Yellow text with bigger font size -->
    <span class="text-3xl font-semibold text-yellow-200">CHARD BIACULO</span>
  </NavBrand>

  <!-- Hamburger for mobile -->
  <NavHamburger />

  <!-- Nav Menu Items with hover effect -->
  <NavUl class="flex space-x-8 items-center bg-transparent">
    <NavLi href="/" active={true} class="text-yellow-200 text-3xl transition transform hover:scale-105 hover:text-yellow-300">Home</NavLi>
    <NavLi href="/portfolio-page" class="text-yellow-200 text-3xl transition transform hover:scale-105 hover:text-yellow-300">Portfolio</NavLi>
    <NavLi href="/about-page" class="text-yellow-200 text-3xl transition transform hover:scale-105 hover:text-yellow-300">About</NavLi>
  </NavUl>
</Navbar>

