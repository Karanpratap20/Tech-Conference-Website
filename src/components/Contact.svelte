<script>
    import { onMount } from "svelte";
    import { writable } from "svelte/store";
    import Header from "./Header.svelte";
  
    let name = writable("");
    let email = writable("");
    let message = writable("");
    let successMessage = writable("");
  
    function handleSubmit(event) {
      event.preventDefault();
      successMessage.set("Your message has been sent successfully!");
      name.set("");
      email.set("");
      message.set("");
    }
  </script>
  
<section>
    <Header />
    <div class="flex items-center justify-center min-h-screen bg-gray-100 dark:bg-gray-900">
        <div class="bg-white dark:bg-gray-800 p-8 rounded-lg shadow-lg w-full max-w-md">
          <h2 class="text-2xl font-semibold text-gray-800 dark:text-white mb-4 text-center">Contact Us</h2>
          
          {#if $successMessage}
            <p class="text-green-500 text-sm text-center mb-4">{$successMessage}</p>
          {/if}
      
          <form on:submit={handleSubmit} class="space-y-4">
            <div>
              <label for="name" class="block text-gray-700 dark:text-gray-300">Name</label>
              <input id="name" bind:value={$name} type="text" required class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500 dark:bg-gray-700 dark:border-gray-600 dark:text-white" placeholder="Your Name" />
            </div>
            <div>
              <label for="mail" class="block text-gray-700 dark:text-gray-300">Email</label>
              <input id="mail" bind:value={$email} type="email" required class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500 dark:bg-gray-700 dark:border-gray-600 dark:text-white" placeholder="Your Email" />
            </div>
            <div>
              <label for="mess" class="block text-gray-700 dark:text-gray-300">Message</label>
              <textarea id="mess" bind:value={$message} required class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500 dark:bg-gray-700 dark:border-gray-600 dark:text-white" rows="4" placeholder="Your Message"></textarea>
            </div>
            <button type="submit" class="w-full bg-indigo-600 hover:bg-indigo-700 text-black py-2 px-4 rounded-lg font-semibold bg-[#181b34]">Send Message</button>
          </form>
        </div>
      </div>
      
</section>