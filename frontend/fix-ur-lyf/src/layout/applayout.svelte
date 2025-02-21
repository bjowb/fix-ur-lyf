<script lang="ts">
  import Navbar from "../components/navbar.svelte";
  import Sidebar from "../components/sidebar.svelte";
  
  let isOpen = false; // Make sure the variable matches Sidebar.svelte prop name
  const toggleSidebar = () => (isOpen = !isOpen);
  const closeSidebar = () => (isOpen = false);
</script>

<div class="flex h-screen">
  <Sidebar {isOpen} {closeSidebar} />
  
  <div class="flex-1">
    <Navbar {toggleSidebar} />
    <main class="mt-16 p-4"> <!-- Ensures content starts below navbar -->
      <slot />
    </main>
  </div>
</div>
