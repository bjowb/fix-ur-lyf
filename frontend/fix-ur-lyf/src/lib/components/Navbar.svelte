<script>
    let links = [
      { name: "Dashboard", href: "/" },
      { name: "Tasks", href: "/tasks" },
      { name: "Calendar", href: "/calendar" }
    ];
  </script>
  
  <nav class="bg-blue-600 text-white p-4 shadow-md">
    <ul class="flex gap-4">
      {#each links as link}
        <li>
          <a href={link.href} class="hover:text-blue-200">{link.name}</a>
        </li>
      {/each}
    </ul>
  </nav>
  