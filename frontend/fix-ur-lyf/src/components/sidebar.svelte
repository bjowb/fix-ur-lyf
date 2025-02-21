<script>
    let selected = "All Tasks";
</script>
  
  <div class="w-64 h-screen bg-gray-900 text-white flex flex-col p-4">
    <!-- App Title -->
    <h1 class="text-xl font-bold flex items-center">
      ✅ Tasks
    </h1>
  
    <!-- Create Button -->
    <button class="mt-4 w-full bg-blue-500 text-white py-2 px-4 rounded-lg hover:bg-blue-600">
      + Create
    </button>
  
    <!-- Task Categories -->
    <div class="mt-6">
      <button class={`w-full text-left py-2 px-2 rounded-lg flex items-center ${
        selected === "All Tasks" ? "bg-blue-600" : "hover:bg-gray-700"
      }`} on:click={() => selected = "All Tasks"}>
        All Tasks
      </button>
      
      <button class={`w-full text-left py-2 px-2 rounded-lg flex items-center ${
        selected === "Starred" ? "bg-blue-600" : "hover:bg-gray-700"
      }`} on:click={() => selected = "Starred"}>
        ⭐ Starred
      </button>
    </div>
  
    <!-- Task Lists -->
    <div class="mt-4">
      <h2 class="text-sm text-gray-400">Lists</h2>
      <button class="w-full text-left py-2 px-2 rounded-lg hover:bg-gray-700 flex items-center">
        📌 My Tasks
      </button>
      <button class="w-full text-left py-2 px-2 rounded-lg hover:bg-gray-700 flex items-center text-blue-400">
        + Create new list
      </button>
    </div>
  </div>
  