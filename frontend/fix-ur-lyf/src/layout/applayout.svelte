<script>
    import Sidebar from "../components/sidebar.svelte";
    import TaskView from "../components/taskview.svelte";
    import NavBar from "../components/navbar.svelte";

    let bool1 = false
    const togglesidebar = () =>{
      bool1 = !bool1
    };
  </script>
  
  <div class="flex h-screen">
    <NavBar {togglesidebar} />
    {#if bool1}
      <Sidebar />
    {/if}
    <TaskView />
  </div>
  