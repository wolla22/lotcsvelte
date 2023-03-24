<script>
  // Replace this with the actual data fetched from your forum API or database
  const announcementPosts = [
    { title: "Announcement 1", author: "User1", timestamp: "2023-03-01" },
    { title: "Announcement 2", author: "User2", timestamp: "2023-03-02" },
    { title: "Announcement 3", author: "User3", timestamp: "2023-03-03" },
    { title: "Announcement 4", author: "User4", timestamp: "2023-03-04" },
    { title: "Announcement 5", author: "User5", timestamp: "2023-03-05" },
  ];
</script>

<style>
  .topics {
    background-color: #222;
    border-radius: 5px;
    padding-left: 1%;
    padding-right: 1%;
    padding-bottom: 1%;
    padding-top: 0.1%;
    font-family: Arial, sans-serif;
    margin-left: 2%; 
    margin-right: 2%;
  }

  .topics-title {
    color: #fff;
    font-size: 1.25rem;
    margin-bottom: 1rem;
  }

  .topic {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #fff;
    margin-bottom: 0.5rem;
    padding: .2%;
  }

  .topic:last-child {
    margin-bottom: 0;

  }

  .topic-title {
    font-size: 1rem;
  }

  .topic-author {
    font-size: 0.9rem;
  }

  .topic-timestamp {
    font-size: 0.9rem;
    color: #aaa;
  }
</style>

<div class="topics">
  <h3 class="topics-title">Latest Announcements</h3>
  {#each announcementPosts as post}
    <div class="topic">
      <div class="topic-title">{post.title}</div>
      <div>
        <span class="topic-author">by {post.author}</span>
        <span class="topic-timestamp"> • {post.timestamp}</span>
      </div>
    </div>
  {/each}
</div>
