<script>
    let isOpen = false;
  </script>
  
  <nav class="bg-gray-900 text-white shadow-md">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16 items-center">
        <!-- Left: Logo -->
        <div class="flex items-center">
          <span class="text-xl font-bold">✅ fix-ur-lyf</span>
        </div>
  
        <!-- Center: Navigation Links (Hidden in Mobile) -->
        <div class="hidden md:flex space-x-6">
          <a href="/" class="hover:text-blue-400">Home</a>
          <a href="/tasks" class="hover:text-blue-400">Tasks</a>
          <a href="/about" class="hover:text-blue-400">About</a>
        </div>
  
        <!-- Right: Menu Button (Mobile) -->
        <div class="md:hidden">
          <button class="focus:outline-none" on:click={() => isOpen = !isOpen}>
            <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              {#if isOpen}
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
              {:else}
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
              {/if}
            </svg>
          </button>
        </div>
      </div>
    </div>
  
    <!-- Mobile Menu -->
    {#if isOpen}
      <div class="md:hidden bg-gray-800">
        <a href="/" class="block py-2 px-4 text-gray-300 hover:bg-gray-700">Home</a>
        <a href="/tasks" class="block py-2 px-4 text-gray-300 hover:bg-gray-700">Tasks</a>
        <a href="/about" class="block py-2 px-4 text-gray-300 hover:bg-gray-700">About</a>
      </div>
    {/if}
  </nav>
  