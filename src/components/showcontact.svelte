<script>
  import { Drawer, Button, CloseButton, Label, Input, Textarea, P, A } from 'flowbite-svelte';
  import { InfoCircleSolid } from 'flowbite-svelte-icons';
  import { sineIn } from 'svelte/easing';

  let hidden3 = true;
  let transitionParams = {
    x: -320,
    duration: 200,
    easing: sineIn
  };
</script>

<div class="text-center mt-8">
  <Button class="bg-white text-gray-800 border border-gray-300 hover:bg-gray-100" pill size="lg" on:click={() => (hidden3 = false)}>Collaborate?</Button>
</div>

<Drawer transitionType="fly" {transitionParams} bind:hidden={hidden3} id="sidebar3" class="bg-white bg-opacity-50 dark:bg-gray-800 dark:bg-opacity-50 shadow-lg rounded-lg p-6 max-w-md backdrop-blur-lg">
  <div class="flex justify-between items-center mb-6">
    <h5 id="drawer-label" class="inline-flex items-center text-lg font-bold text-gray-900 dark:text-gray-100">
      <InfoCircleSolid class="w-6 h-6 me-2.5" /> Contact Us
    </h5>
    <CloseButton on:click={() => (hidden3 = true)} class="dark:text-gray-300" />
  </div>
  
  <form action="#" class="space-y-6">
    <div>
      <Label for="email" class="block text-sm font-medium text-gray-700 dark:text-gray-300">Your email</Label>
      <Input id="email" name="email" required placeholder="name@company.com" class="mt-1 p-2 block w-full rounded-md border-gray-300 shadow-sm focus:ring-gray-500 focus:border-gray-500 dark:bg-gray-900 dark:border-gray-700" />
    </div>
    <div>
      <Label for="subject" class="block text-sm font-medium text-gray-700 dark:text-gray-300">Subject</Label>
      <Input id="subject" name="subject" required placeholder="Let us know how we can help you" class="mt-1 p-2 block w-full rounded-md border-gray-300 shadow-sm focus:ring-gray-500 focus:border-gray-500 dark:bg-gray-900 dark:border-gray-700" />
    </div>
    <div>
      <Label for="message" class="block text-sm font-medium text-gray-700 dark:text-gray-300">Your message</Label>
      <Textarea id="message" name="message" rows="4" placeholder="Your message..." class="mt-1 p-2 block w-full rounded-md border-gray-300 shadow-sm focus:ring-gray-500 focus:border-gray-500 dark:bg-gray-900 dark:border-gray-700" />
    </div>
    <Button color="yellow" pill type="submit" class="w-full bg-white text-gray-800 border border-gray-300 hover:bg-gray-100 focus:ring-4 focus:ring-gray-300 dark:focus:ring-gray-700">Send message</Button>
  </form>
  
  <P class="mt-4 text-sm text-gray-600 dark:text-gray-400">
    Need immediate help? Email us at <A href="mailto:202211449@gordoncollege.edu.ph" class="text-gray-600 hover:underline dark:text-gray-400">202211449@gordoncollege.edu.ph</A>
  </P>
  <P class="text-sm text-gray-600 dark:text-gray-400">
    Or call us at <A href="tel:+639266792206" class="text-gray-600 hover:underline dark:text-gray-400">09266792206</A>
  </P>
</Drawer>
