<script setup>
// This is just a placeholder for user's login status.
// In a real application you would get the actual login status of the user.
let isLoggedIn = ref(false);

const logout = () => {
  isLoggedIn.value = false;
  // Here you would add your logout logic
};

const login = () => {
  isLoggedIn.value = true;
  // Here you would add your login logic
};
</script>

<template>
  <nav
    class="fixed top-0 left-0 w-full bg-white shadow-md p-4 flex justify-between items-center"
  >
    <div>
      <img
        src="/imgs/taller-de-artes-logo.svg"
        alt="Taller de Artes Online"
        class="md:w-[8ch] w-[6ch]"
      />
    </div>
    <div class="flex space-x-4">
      <a href="#" class="hover:text-blue-500">About</a>
      <a href="#" class="hover:text-blue-500">FAQ</a>
      <a href="#" class="hover:text-blue-500">Contact</a>
    </div>
    <div>
      <button
        v-if="isLoggedIn"
        @click="logout"
        class="bg-red-500 text-white py-1 px-2 rounded"
      >
        Log Out
      </button>
      <button
        v-else
        @click="login"
        class="bg-green-500 text-white py-1 px-2 rounded"
      >
        Log In
      </button>
    </div>
  </nav>
</template>
