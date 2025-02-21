<script lang="ts">
  export let isOpen: boolean;
  export let closeSidebar: () => void;
</script>

<!-- Overlay (for clicking outside) -->
{#if isOpen}
  <div class="fixed inset-0 bg-black bg-opacity-50 z-40" on:click={closeSidebar}></div>
{/if}

<!-- Sidebar -->
<div class={`fixed top-0 left-0 w-64 bg-gray-800 text-white h-full shadow-md transform 
  ${isOpen ? 'translate-x-0' : '-translate-x-full'} transition-transform duration-300 ease-in-out z-50`}>
  
  <div class="p-5 flex justify-between items-center border-b border-gray-700">
    <span class="text-lg font-semibold">Menu</span>
    <button class="text-gray-300 hover:text-white" on:click={closeSidebar}>✖</button>
  </div>

  <ul class="mt-4 space-y-2 p-4">
    <li><a href="/" class="block py-2 px-4 hover:bg-gray-700 rounded">Home</a></li>
    <li><a href="/tasks" class="block py-2 px-4 hover:bg-gray-700 rounded">Tasks</a></li>
    <li><a href="/about" class="block py-2 px-4 hover:bg-gray-700 rounded">About</a></li>
  </ul>
</div>
