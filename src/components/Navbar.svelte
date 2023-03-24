<script>
  let menuOpen = false;

  function toggleMenu() {
    menuOpen = !menuOpen;
  }
</script>

<style>
  .navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #333;
    padding: 1rem;
    font-family: Arial, sans-serif;
  }

  .navbar-brand {
    color: #fff;
    font-size: 1.5rem;
    text-decoration: none;
  }

  .navbar-menu {
    display: flex;
    gap: 1rem;
  }

  .navbar-menu a {
    color: #fff;
    text-decoration: none;
    transition: color 0.2s;
  }

  .navbar-menu a:hover {
    color: #ccc;
  }

  .menu-toggle {
    display: none;
    cursor: pointer;
  }

  .menu-toggle img {
    height: 1.5rem;
  }

  @media (max-width: 768px) {
    .navbar-menu {
      display: none;
    }

    .menu-toggle {
      display: block;
    }

    .navbar-menu.open {
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
      position: absolute;
      top: 100%;
      left: 0;
      background-color: #333;
      padding: 1rem;
      width: 100%;
    }
  }
</style>

<nav class="navbar">
  <div class="navbar-menu {menuOpen ? 'open' : ''}">
    <a href="/home">Home</a>
    <a href="/forums">Forums</a>
    <a href="/wiki">Wiki</a>
    <a href="/apply">Apply</a>
    <a href="/store">Store</a>
    <a href="/support">Support</a>
  </div>
  <div class="menu-toggle" on:click={toggleMenu}>
    <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOEAAADhCAMAAAAJbSJIAAAAYFBMVEX///8AAADPz89LS0uWlpb5+fmFhYXHx8eSkpJnZ2ezs7Oqqqp3d3cWFhbk5OT19fU/Pz9aWlra2tqkpKTu7u4PDw+9vb1gYGB9fX0zMzMkJCQaGhqbm5s4ODjLy8tQUFACQSuFAAACZ0lEQVR4nO3d7VLCMBCF4VipfKMiAorI/d+lVmHQP7spyczObt/nCs4Za7RhSVICAAAAAAAAAAAAAAAAgAEYT6b3fkwn4371Nvs7f/ab/IIT67A3mmT2a4/WSW92bLMKLq1zFljmVHyzTlnkTS/4YJ2x0INWcGWdsNhKaTi1DlhsKhd8tM5XwaPYcGYdr4KZ2HBhHa+ChdjwyTpeBU9iw1freBW8ig2t01UhNny3TlfBu9jw2TpeBc9iw5F1vApGYsPGOl4FjdgwwGIqL6Upza0DFpsrDdPBOmGhg1Ywra0jFlqrDZ0/p+oz2nmxTlngJadgSmPrnDfL3hZufb5ELbL2Es82H942TY8fPba8z1aNH9r2EwAAAAAAAAAA8Kz9nI/8mH/2+dypsz1Zf5bU22nbo1/jc1zhoEzSXPkdZlfH2H/trHMW2OUU9PkJ94U8IPzD+6S3POX9rbVOWEz7s+F3lbnQVhvrfBXIBf0OC13JY0P+H1LtMb23jlfBSWzo+duVF0uxoXW6Kgb+M4z/exh/LY3/9zDCUiMXDPCYav+Xxn+3iP9+OIB3/AHs03hebTL32lJqfH5ZNn+/NMXf8+5E/9wCAAAAAAAAAAB4EvucqOhnfYU/r83v2FDmmXvhz00Mf/Zl/PNLfX6p60o9g9b3M9rRntPwZ0HHP8/b611Wf8lnssc/V9/nuNd/8t0I1umqEBv6X0q1xTT+PTM+X5v+k8eEvU95d+RJ7/h3dsW/d20Ad+c5HmP/lTHMHv4OywHcQxr/Ltnk9x0q9z7gNIA7nTvB7+UGAAAAAAAAAAAAAAAAAJ++ACLpVB+zWmM6AAAAAElFTkSuQmCC" alt="Menu icon" />
  </div>
</nav>
