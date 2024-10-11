<script>
    import { GradientButton, Modal } from 'flowbite-svelte';
    import { QuestionCircleOutline } from 'flowbite-svelte-icons';
    let FacebookIcon     = "../images/facebook.png"; 
    let InstagramIcon    = "../images/instagram.png";  
    let LinkedInIcon     = "../images/linkedin.png"; 
    let GoogleIcon       = "../images/gmail.png";
    
    let socialMediaModal = false;
  </script>
  <div>
  <GradientButton on:click={() => (socialMediaModal = true)} color="tealToLime">Connect with Social Media</GradientButton>
</div>
  <Modal title="Connect with Social Media" bind:open={socialMediaModal} size="xs">
    <p class="text-sm font-normal text-gray-500 dark:text-gray-400">
      Connect with one of our social media accounts to proceed.
    </p>    
    
    <ul class="my-4 space-y-3">
      <li>
        <a href="https://www.facebook.com/richard.biaculo" target="_blank" class="flex items-center p-3 text-base font-bold text-gray-900 bg-gray-50 rounded-lg hover:bg-gray-100 group hover:shadow dark:bg-gray-600 dark:hover:bg-gray-500 dark:text-white">
          <img src={FacebookIcon} alt="Facebook" class="w-6 h-6" />  
          <span class="flex-1 ms-3 whitespace-nowrap">Facebook</span>
        </a>
      </li>
      <li>
        <a href="https://www.instagram.com" target="_blank" class="flex items-center p-3 text-base font-bold text-gray-900 bg-gray-50 rounded-lg hover:bg-gray-100 group hover:shadow dark:bg-gray-600 dark:hover:bg-gray-500 dark:text-white">
          <img src={InstagramIcon} alt="Instagram" class="w-6 h-6" />
          <span class="flex-1 ms-3 whitespace-nowrap">Instagram</span>
        </a>
      </li>
      <li>
        <a href="https://www.linkedin.com" target="_blank" class="flex items-center p-3 text-base font-bold text-gray-900 bg-gray-50 rounded-lg hover:bg-gray-100 group hover:shadow dark:bg-gray-600 dark:hover:bg-gray-500 dark:text-white">
          <img src={LinkedInIcon} alt="LinkedIn" class="w-6 h-6" />
          <span class="flex-1 ms-3 whitespace-nowrap">LinkedIn</span>
        </a>
      </li>
      <li>
        <a href="mailto:202211927@gordoncollege.edu.ph" class="flex items-center p-3 text-base font-bold text-gray-900 bg-gray-50 rounded-lg hover:bg-gray-100 group hover:shadow dark:bg-gray-600 dark:hover:bg-gray-500 dark:text-white">
          <img src={GoogleIcon} alt="Google" class="w-6 h-6" />
          <span class="flex-1 ms-3 whitespace-nowrap">Google</span>
        </a>
      </li>
    </ul>
  
    <div>
      <a href="/" class="inline-flex items-center text-xs font-normal text-gray-500 hover:underline dark:text-gray-400">
        <QuestionCircleOutline class="w-3 h-3 me-2" /> Why do I need to connect with a social media account?
      </a>
    </div>
  </Modal>
  