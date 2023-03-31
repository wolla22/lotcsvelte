<script>
    import Header from '../components/Header.svelte';
    import Navbar from '../components/Navbar.svelte';
    import Subheader from '../components/Subheader.svelte';
    import Banner from '../components/Banner.svelte';
    import Sidebar from '../components/Sidebar.svelte';
    import Topics from '../components/Topics.svelte';
</script>

<head>
    <style>
        body {
            margin: 0;
            background-color:#333;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2%;
        }
        .main {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: flex-start;
        }
        .content {
            flex: 2;
            display: flex;
            flex-direction: column;
            align-items: left;
        }
        .sidebar {
            align-items: right
            flex: 1;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
    </style>
</head>

<body>
  <Header />
  <Navbar />
  <Subheader />
  <div class="container">
    <div class="main">
      <div class="content">
        <Banner />
        <Topics />
      </div>
      <div class="sidebar">
        <Sidebar />
      </div>
    </div>
  </div>
</body>
