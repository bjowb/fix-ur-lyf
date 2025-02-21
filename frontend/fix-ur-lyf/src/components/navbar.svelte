<script lang="ts">
  export let toggleSidebar: () => void;
</script>

<nav class="bg-gray-900 text-white shadow-md fixed w-full z-50">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between h-16 items-center">
      <!-- Logo (Click to Open Sidebar) -->
      <div class="flex items-center space-x-2 cursor-pointer" on:click={toggleSidebar}>
        <span class="text-green-400 text-2xl font-bold">✅ fix-ur-lyf</span>
      </div>

      <!-- Navigation Links (Hidden in Mobile) -->
      <div class="hidden md:flex space-x-6">
        <a href="/" class="hover:text-blue-400">Home</a>
        <a href="/tasks" class="hover:text-blue-400">Tasks</a>
        <a href="/about" class="hover:text-blue-400">About</a>
      </div>
    </div>
  </div>
</nav>
