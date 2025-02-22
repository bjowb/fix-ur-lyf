<script lang="ts">
  export let toggleSidebar: () => void;
  import { buttonVariants } from "$lib/components/ui/button";
</script>

<nav class="bg-[#111111] text-[#4caf50] shadow-md fixed w-full z-50">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex justify-between h-16 items-center">
      <!-- Logo (Click to Open Sidebar) -->
      <div class="flex items-center space-x-2 cursor-pointer" on:click={toggleSidebar}>
        <span class="text-[#4caf50] text-2xl font-bold">fix-ur-lyf</span>
      </div>
      <!-- Navigation Links (Hidden in Mobile) -->
      <div class="hidden md:flex space-x-6 text-[20px]">
        <a href="/" class={buttonVariants({ variant: "outline" })}>
          home
        </a>
        <a href="/tasks" class={buttonVariants({ variant: "outline" })}>
          tasks
        </a>
        <a href="/about" class={buttonVariants({ variant: "outline" })}>
          about
        </a>
      </div>
    </div>
  </div>
</nav>

<style>
  /* Component-specific styles can go here */
</style>
