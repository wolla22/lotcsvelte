<script>
  let createDropdownOpen = false;
  let accountDropdownOpen = false;

  function toggleCreateDropdown() {
    createDropdownOpen = !createDropdownOpen;
  }

  function toggleAccountDropdown() {
    accountDropdownOpen = !accountDropdownOpen;
  }
</script>

<style>
  .header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #222;
    padding: 0.5rem 1rem;
    font-family: Arial, sans-serif;
  }

  .header-title {
    color: #fff;
    font-size: 1.75rem;
    margin: 0.5%;
  }

  .header-tools {
    display: flex;
    align-items: center;
    gap: 1rem;
  }

  .dropdown {
    position: relative;
  }

  .dropdown-toggle {
    color: #fff;
    cursor: pointer;
  }

  .dropdown-menu {
    display: none;
    position: absolute;
    top: 100%;
    right: 0;
    background-color: #333;
    padding: 0.5rem;
    border-radius: 5px;
    min-width: 200px;
  }

  .dropdown-menu.open {
    display: block;
  }

  .dropdown-menu a {
    display: block;
    color: #fff;
    text-decoration: none;
    padding: 0.25rem 0;
  }

  .dropdown-menu a:hover {
    color: #ccc;
  }

  .icon {
    color: #fff;
    cursor: pointer;
  }
</style>

<header class="header">
  <h1 class="header-title">The Lord of the Craft</h1>
  <div class="header-tools">
    <div class="dropdown">
      <span class="dropdown-toggle" on:click={toggleCreateDropdown}>Create New Content</span>
      <div class="dropdown-menu {createDropdownOpen ? 'open' : ''}">
        <a href="/status">Status</a>
        <a href="/application">Application in Personas</a>
        <a href="/topic">Topic</a>
        <a href="/submit-form">Submit Form</a>
      </div>
    </div>
    <span class="icon">🔔</span> <!-- Replace with your preferred notifications icon -->
    <span class="icon">✉️</span> <!-- Replace with your preferred messages icon -->
    <div class="dropdown">
      <span class="dropdown-toggle" on:click={toggleAccountDropdown}>Account Information</span>
      <div class="dropdown-menu {accountDropdownOpen ? 'open' : ''}">
        <a href="/profile">Profile</a>
        <a href="/settings">Settings</a>
        <a href="/logout">Logout</a>
      </div>
    </div>
  </div>
</header>
