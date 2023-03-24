<script>
  let currentPage = "Home"; // Replace this with logic to determine the current page
</script>

<style>
  .subheader {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #222;
    padding: 0.5rem 1rem;
    font-family: Arial, sans-serif;
  }

  .current-page {
    color: #fff;
    font-size: 1.25rem;
    margin: 0;
  }

  .subheader-tools {
    display: flex;
    gap: 1rem;
  }

  .subheader-tools a {
    color: #fff;
    text-decoration: none;
    font-size: 1.1rem;
  }

  .subheader-tools a:hover {
    color: #ccc;
  }
</style>

<div class="subheader">
  <h2 class="current-page">{currentPage}</h2>
  <div class="subheader-tools">
    <a href="/unread-content">Unread Content</a>
    <a href="/mark-site-read">Mark site read</a>
  </div>
</div>