<script lang="ts">
  import lottie from "lottie-web";
  import { onMount } from "svelte";
  import ThemeSwitch from "./ThemeSwitch.svelte";
  import Button from "./ui/button/button.svelte";

  const links = [
    { text: "About me", href: "./" },
    { text: "Resume", href: "./resume" },
    { text: "Projects", href: "./projects" },
    { text: "Contact", href: "./contact" },
  ];

  onMount(() => {
    const toggleButton = document.querySelector('.toggle') as HTMLElement | null;
    const slide = document.querySelector('.slide') as HTMLElement | null;

    if (toggleButton && slide) {
      toggleButton.addEventListener('click', () => {
        if (slide.classList.contains('hidden')) {
          // Show the slide
          slide.classList.remove('hidden');
          slide.style.display = 'flex';
          requestAnimationFrame(() => {
            slide.style.transform = 'translateX(0)';
            slide.style.opacity = '1';
          });
        } else {
          // Hide the slide with animation first
          slide.style.transform = 'translateX(300px)';
          slide.style.opacity = '0';
          
          // After the transition, hide the element
          slide.addEventListener('transitionend', () => {
            slide.style.display = 'none';
            slide.classList.add('hidden');
            // Reset transform and opacity to avoid accumulated effects
            slide.style.transform = '';
            slide.style.opacity = '';
          }, { once: true });
        }
      });
      
      // Initial state
      slide.style.transform = 'translateX(300px)';
      slide.style.opacity = '0';
      slide.style.display = 'none'; // Make sure it's hidden initially
    }
  });
</script>

<div class="px-6 py-6 w-full">
  <nav
    class="text-3xl font-bold hover:font-black flex justify-between items-center"
  >
    <a href="./" class="logo text-3xl font-bold text-shadow hover:scale-105 p-2">
      GA
    </a>

    <div class="nav-bar flex items-center uppercase">
      <span class="hidden md:flex ml-1">
        {#each links as link}
          <Button href={link.href} variant="link" class="text-lg ml-8 mr-8">
            {link.text}
          </Button>
        {/each}

        <ThemeSwitch />
      </span>

      

    <div class="flex md:hidden ml-1">
      <label>
        <input type="checkbox">
        <div class="toggle">
          <span class="top_line common"></span>
          <span class="middle_line common"></span>
          <span class="bottom_line common"></span>
        </div>
        <div class="slide hidden">
          <h1>menu</h1>
          <ul>
            <li><a href="./"><i class="fas fa-user"></i>About me</a></li>
            <li><a href="./resume"><i class="fas fa-file-alt"></i>Resume</a></li>
            <li><a href="./projects"><i class="fas fa-code"></i>Projects</a></li>
            <li><a href="./contact"><i class="fas fa-envelope"></i>Contact</a></li>
          </ul>
        </div>
      </label>
    </div>
  </nav>
</div>
