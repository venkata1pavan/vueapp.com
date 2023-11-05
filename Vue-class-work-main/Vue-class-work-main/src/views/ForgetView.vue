<template>
    <div class="min-h-screen flex items-center justify-center px-4 sm:px-6 lg:px-8 mb-22">
      <div class="max-w-md w-full">
        <h1 class="text-3xl font-bold mb-6">Forget Password</h1>
        <form class="space-y-4">
          <div>
            <label for="email" class="block text-sm font-medium">Email</label>
            <input type="email" id="email" name="email" class="mt-1 block w-full rounded-md shadow-sm">
          </div>
          <div>
            <button type="submit" class="w-full py-2 px-4 border border-transparent rounded-md shadow-sm text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
              Send Reset Email
            </button>
          </div>
        </form>
  
        <!-- Go back to login link -->
        <div class="mt-4 text-sm">
          <router-link to="/login" class="text-indigo-600">Go back to login</router-link>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  // Your script setup code (if any)
  </script>
  
  