<script lang="ts">
    import { onMount } from "svelte";
  import ThemeSwitch from "./ThemeSwitch.svelte";
  import Button from "./ui/button/button.svelte";

  let y = 0;

function handleScroll() {
  y = window.scrollY;
}

onMount(() => {
  window.addEventListener('scroll', handleScroll);
  return () => window.removeEventListener('scroll', handleScroll);
});
  const links = [
    { text: "Home", href: "./" },
    { text: "Resume", href: "./resume" },
    { text: "Contact", href: "./contact" },
  ];
</script>

  <nav
  class={" w-full sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid " +
  (y > 0
    ? " py-4 bg-[#080b1a] border-[#425173]"
    : " py-6 bg-transparent border-transparent")}
    >
    <!-- class="text-3xl font-bold hover:font-black flex justify-between items-center" -->

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
            class={`text-xl ${link.text === "Home" ? "mr-5" : "mr-9"} ml-8`}
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
                <a href="./contact"><i class="fas fa-envelope"></i>Contact</a>
              </li>
            </ul>
          </div>
        </label>
      </div>
    </div>
  </nav>
