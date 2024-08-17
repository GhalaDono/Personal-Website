<script lang="ts">
  import ThemeSwitch from "./ThemeSwitch.svelte";
  import Button from "./ui/button/button.svelte";

  const links = [
    { text: "Home", href: "./" },
    { text: "Resume", href: "./resume" },
    { text: "Projects", href: "./projects" },
    { text: "Contact", href: "./contact" },
  ];
</script>

<div class="px-6 py-10 w-full">
  <nav
    class="text-3xl font-bold hover:font-black flex justify-between items-center"
  >
    <a
      href="./"
      class="logo text-3xl font-bold text-shadow hover:scale-105 p-2"
    >
      GA
    </a>

    <div class="nav-bar flex items-center uppercase">
      <span class="hidden md:flex ml-1">
        {#each links as link}
        <Button 
          href={link.href} 
          variant="link" 
          class={`text-lg ${link.text === 'Home' ? 'ml-0' : link.text === 'Resume' ? 'ml-4 mr-0' : link.text === 'Projects' ? 'ml-8' : 'ml-9'} mr-8`}
        >
          {link.text}
        </Button>
      {/each}

        <ThemeSwitch />
      </span>

      <div class="flex md:hidden ml-1">
        <label>
          <input type="checkbox" />
          <div class="toggle bg-[#080b1a]">
            <span class="top_line common"></span>
            <span class="middle_line common"></span>
            <span class="bottom_line common"></span>
          </div>
          <div class="slide hidden">
            <h1>menu</h1>
            <ul>
              <li><a href="./"><i class="fas fa-home"></i>Home</a></li>
              <li>
                <a href="./resume"><i class="fas fa-file-alt"></i>Resume</a>
              </li>
              <li>
                <a href="./projects"><i class="fas fa-code"></i>Projects</a>
              </li>
              <li>
                <a href="./contact"><i class="fas fa-envelope"></i>Contact</a>
              </li>
            </ul>
          </div>
        </label>
      </div>
    </div>
  </nav>
</div>
