<template>
  <div class="bg-black py-10 px-4 sm:px-8 md:px-16 lg:px-24 xl:px-32 mt-24">
    <h1 class="text-3xl font-bold mb-6 text-center">Contact Us</h1>

    <!-- Contact Section -->
    <div class="flex flex-col sm:flex-row justify-center items-center">
      <!-- Map on the left -->
      <div class="w-full sm:w-1/2 p-4">
        <!-- Replace the map iframe with your embedded map -->
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3988.934856523896!2d36.81580901456491!3d-1.2592995990236034!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x182f1826c0d98c71%3A0x509771ed2a4dcd5b!2sParklands%2C%20Nairobi!5e0!3m2!1sen!2ske!4v1628461871412!5m2!1sen!2ske"
          width="100%"
          height="300"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
        ></iframe>
      </div>

      <!-- Form on the right -->
      <div class="w-full sm:w-1/2 p-4">
        <form class="bg-black rounded-lg shadow-md p-6">
          <h2 class="text-xl font-bold mb-4">Get in Touch</h2>
          <div class="mb-4">
            <label for="name" class="block text-sm font-bold mb-2">Name:</label>
            <input
              type="text"
              id="name"
              name="name"
              placeholder="Enter your name"
              class="w-full border border-gray-300 rounded-md p-2"
            />
          </div>
          <div class="mb-4">
            <label for="email" class="block text-sm font-bold mb-2">Email:</label>
            <input
              type="email"
              id="email"
              name="email"
              placeholder="Enter your email"
              class="w-full border border-gray-300 rounded-md p-2"
            />
          </div>
          <div class="mb-4">
            <label for="message" class="block text-sm font-bold mb-2">Message:</label>
            <textarea
              id="message"
              name="message"
              placeholder="Enter your message"
              rows="4"
              class="w-full border border-gray-300 rounded-md p-2"
            ></textarea>
          </div>
          <button
            type="submit"
            class="bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-2 px-4 rounded-full"
          >
            Send Message
          </button>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
// Your script setup code here
</script>

<style scoped>
/* Your styles here */
</style>
