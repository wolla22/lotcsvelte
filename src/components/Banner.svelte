<script>
  import { onMount } from 'svelte';

  let slideIndex = 0;

  function showSlides() {
    const slides = document.getElementsByClassName('slide');
    for (let i = 0; i < slides.length; i++) {
      slides[i].style.display = 'none';
    }

    if (slideIndex > slides.length) {
      slideIndex = 1;
    } else if (slideIndex < 1) {
      slideIndex = slides.length;
    }

    slides[slideIndex - 1].style.display = 'block';
  }

  function nextSlide() {
    slideIndex++;
    showSlides();
  }

  function previousSlide() {
    slideIndex--;
    showSlides();
  }

  onMount(() => {
    showSlides();
    setInterval(nextSlide, 5000); // Change image every 5 seconds
  });
</script>


<style>
  .banner {
    display: flex;
    overflow: hidden;
    flex-wrap: wrap;
    margin: 1%;
  }

  .banner-container {
    position: relative;
    width: 100%;
    height: 400px;
    overflow: hidden;
    margin: 1%;
  }

  .slide {
    position: absolute;
    width: 100%;
    height: 400px;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    transition: opacity 1s;
    display: none;
  }

  .banner-text {
    position: absolute;
    left: 59%;
    bottom: 2%;
    text-align: left;
    color: #fff;
    background: rgba(0, 0, 0, 0.5);
    padding: 0.8rem;
    border-radius: 5px;
    width: 37%;
  }

  .banner-text h1 {
    font-size: 1.3rem;
    margin-bottom: 0.5rem;
  }

  .banner-text p {
    font-size: 1rem;
  }

  .arrow {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    font-size: 2rem;
    color: white;
    cursor: pointer;
    z-index: 1;
  }

  .arrow.left {
    left: 1%;
  }

  .arrow.right {
    right: 1%;
  }
</style>

<div class="banner">
    <div class="banner-container">
      <div class="slide" style="background-image: url('https://cdn.lordofthecraft.net/monthly_2022_09/BANNER-1.jpg.83bbd0856af5fe2e7532693e7a89a844.jpg');"></div>
      <div class="slide" style="background-image: url('https://cdn.lordofthecraft.net/monthly_2022_09/BANNER-2.jpg.c82b1ec48aec0e1b0851ccd47427a9c8.jpg');"></div>
      <div class="slide" style="background-image: url('https://cdn.lordofthecraft.net/monthly_2022_09/BANNER-3.jpg.d46212fb70533be100151e8ac9e28388.jpg');"></div>
      <div class="banner-text">
       <h1>Welcome to Lord of the Craft</h1>
  <p>Join our roleplay server today</p>
</div>
<span class="arrow left" on:click={previousSlide}>&lt;</span>
<span class="arrow right" on:click={nextSlide}>&gt;</span>
</div>
</div>



