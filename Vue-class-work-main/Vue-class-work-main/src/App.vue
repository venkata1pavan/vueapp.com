<template>
  <nav class="bg-slate-900 text-white fixed top-0 left-0 right-0 h-16 flex items-center justify-between px-4 sm:px-8">
    <!-- Logo -->
    <div class="flex items-center">
    <h1 class="text-xl font-bold">
      <span class="text-indigo-600">Twende</span>
      <span class="text-white">Electric</span>
    </h1>
  </div>

    <!-- Desktop navigation -->
    <div class="hidden sm:flex space-x-4 flex-grow justify-center">
      <router-link class="px-4 py-2 font-bold" :class="{'bg-indigo-600': isActive('/')}" to="/">Home</router-link>
      <router-link class="px-4 py-2 font-bold" :class="{'bg-indigo-600': isActive('/about')}" to="/about">About</router-link>
      <router-link class="px-4 py-2 font-bold" :class="{'bg-indigo-600': isActive('/services')}" to="/services">Services</router-link>
      <router-link class="px-4 py-2 font-bold" :class="{'bg-indigo-600': isActive('/contact')}" to="/contact">Contact</router-link>
    </div>

    <!-- Login button -->
    <div class="hidden sm:block">
    <router-link class="px-4 py-2 font-bold bg-indigo-600 rounded-full hover:bg-slate-600" :class="{'text-white': isActive('/login')}" to="/login">Sign in</router-link>
  </div>

    <!-- Mobile navigation (hamburger menu) -->
    <div class="sm:hidden flex justify-end">
      <button @click="toggleMobileMenu" class="px-4 py-2 text-xl text-white">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
        </svg>
      </button>
    </div>

    <!-- Mobile menu items (hidden by default) -->
    <div v-if="showMobileMenu" class="sm:hidden bg-slate-900 absolute top-16 left-0 right-0">
      <router-link @click="toggleMobileMenu" class="block px-4 py-2 font-bold text-white hover:bg-indigo-600" :class="{'bg-indigo-600': isActive('/')}" to="/">Home</router-link>
      <router-link @click="toggleMobileMenu" class="block px-4 py-2 font-bold text-white hover:bg-indigo-600" :class="{'bg-indigo-600': isActive('/about')}" to="/about">About</router-link>
      <router-link @click="toggleMobileMenu" class="block px-4 py-2 font-bold text-white hover:bg-indigo-600" :class="{'bg-indigo-600': isActive('/services')}" to="/services">Services</router-link>
      <router-link @click="toggleMobileMenu" class="block px-4 py-2 font-bold text-white hover:bg-indigo-600" :class="{'bg-indigo-600': isActive('/contact')}" to="/contact">Contact</router-link>
      <router-link @click="toggleMobileMenu" class="block px-4 py-2 font-bold text-white hover:bg-indigo-600" :class="{'bg-indigo-600': isActive('/login')}" to="/login">Login</router-link>
    </div>

  </nav>
  <router-view />
</template>

<script setup>
import { ref } from 'vue';
import { useRoute } from 'vue-router';

const showMobileMenu = ref(false);

const toggleMobileMenu = () => {
  showMobileMenu.value = !showMobileMenu.value;
};

const isActive = (route) => {
  const currentRoute = useRoute();
  return currentRoute.path === route;
};
</script>

<style scoped>
/* Add your custom styles here */
</style>
