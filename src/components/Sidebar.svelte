<script>
  // Replace the values below with the actual data for your application
  let serverIP = "mc.lotc.co";
  let serverVersion = "1.16.5";
  let discordInviteLink = "https://discord.gg/lotc";
  let onlineUsers = ["User1", "User2", "User3"]; // Replace with logic to fetch online users
</script>

<style>
  .sidebar {
    display: flex;
    width: 370px;
    font-family: Arial, sans-serif;
    flex-shrink: 1;
    float: right;
    margin: .5em;
    margin-left: .1em;
    padding-left: 1em;
  }

  .sidebar-section {
    background-color: #222;
    border-radius: 5px;
    padding: .5rem;
    margin-bottom: .5rem;
    width: 90%;
    box-shadow: 1px 1px 4px 0px rgba(0, 0, 0, 0.75);
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
    gap: 0.1rem;
  }

  .online-user {
    color: #fff;
    font-size: 0.9rem;
  }

  @media (max-width: 2000px) {
    .sidebar {
      width: 350px;
    }
  }

  @media (max-width: 1024px) {
    .sidebar {
      width: 250px;
    }
  }

  @media (max-width: 768px) {
    .sidebar {
      width: 200px;
      padding-left: 1.5em;
      margin-left: 0em;
    }
    .sidebar-title {
      font-size: .9rem;
    }
    .sidebar-text {
      font-size: 0.7rem;
    }
    .online-user {
      font-size: 0.5rem;
    }
  }

  @media (max-width: 480px) {
    .sidebar {
      padding-left: 1em;
      margin-left: 0em;
      width: 410px;
      padding-right: 0px;
      margin-right: 0px;
    }
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
        <div class="online-user">{user+", "}</div>
      {/each}
    </div>
  </div>
</div>
