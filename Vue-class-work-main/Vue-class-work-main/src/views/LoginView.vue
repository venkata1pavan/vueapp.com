<template>
  <div class="min-h-screen flex items-center justify-center px-4 sm:px-6 lg:px-8">
    <div class="max-w-md w-full">
      <h1 class="text-3xl font-bold mb-6 text-center">Login</h1>
      <form class="space-y-4">
        <div>
          <label for="username" class="block text-sm font-medium text-center">Username</label>
          <input type="text" id="username" name="username" class="mt-1 block w-full rounded-md shadow-sm">
        </div>
        <div>
          <label for="email" class="block text-sm font-medium text-center">Email</label>
          <input type="email" id="email" name="email" class="mt-1 block w-full rounded-md shadow-sm">
        </div>
        <div>
          <label for="password" class="block text-sm font-medium text-center">Password</label>
          <input type="password" id="password" name="password" class="mt-1 block w-full rounded-md shadow-sm">
        </div>
        <div>
          <button type="submit" class="w-full py-2 px-4 border border-transparent rounded-md shadow-sm text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
            Sign In
          </button>
        </div>
      </form>

      <!-- Don't have an account and Forgot password links -->
      <div class="mt-4 text-sm flex justify-between">
        <router-link to="/signup" class="text-indigo-600">Don't have an account? Sign Up</router-link>
        <router-link to="/forget" class="text-indigo-600">Forgot Password?</router-link>
      </div>
    </div>
  </div>
</template>

