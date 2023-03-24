<script>
  // Replace the values below with the actual data for your application
  let serverIP = "mc.lotc.co";
  let serverVersion = "1.16.5";
  let discordInviteLink = "https://discord.gg/lotc";
  let onlineUsers = ["User1", "User2", "User3"]; // Replace with logic to fetch online users
</script>

<style>
  .sidebar {
    width: 300px;
    font-family: Arial, sans-serif;
    flex-shrink: 1;
    background-color: #222;
    padding: 1em;
    float: right;
  }

  .sidebar-section {
    background-color: #333;
    border-radius: 5px;
    padding: 1rem;
    margin-bottom: 1rem;
    width: 250px;
  }

  .sidebar-title {
    color: #fff;
    font-size: 1.25rem;
    margin-bottom: 1rem;
  }

  .sidebar-text {
    color: #fff;
    font-size: 1rem;
  }

  .online-users-list {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .online-user {
    color: #fff;
    background-color: #444;
    padding: 0.25rem 0.5rem;
    border-radius: 5px;
    font-size: 0.9rem;
  }
</style>

<div class="sidebar">
  <div class="sidebar-section">
    <h3 class="sidebar-title">Server Information</h3>
    <p class="sidebar-text">IP: {serverIP}</p>
    <p class="sidebar-text">Version: {serverVersion}</p>
  </div>
  <div class="sidebar-section">
    <h3 class="sidebar-title">Discord</h3>
    <p class="sidebar-text">
      Join our Discord server: <a href={discordInviteLink}>{discordInviteLink}</a>
    </p>
  </div>
  <div class="sidebar-section">
    <h3 class="sidebar-title">Online Users</h3>
    <div class="online-users-list">
      {#each onlineUsers as user}
        <div class="online-user">{user}</div>
      {/each}
    </div>
  </div>
</div>
