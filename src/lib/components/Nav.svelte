<script>
  import ThemeSwitch from "./ThemeSwitch.svelte";
  import Button from "./ui/button/button.svelte";
</script>

<nav class="text-3xl font-bold hover:font-black flex justify-between items-baseline px-6 py-6 ">
  <a href="./" class="logo text-3xl font-bold text-shadow hover:scale-110">
    GA
  </a>

 

  <div class="flex items-center uppercase">
    <ThemeSwitch /><!-- ./ حطيت نقطة عشاني برفعه على قيتهب -->
    <Button href="./resume" variant="link" class="text-lg ml-6 mr-8 hover:scale-110">Resume</Button>
    <Button href="./projects" variant="link" class="text-lg mx-8 hover:scale-110">Projects</Button>
    <Button href="./contact" variant="link" class="text-lg mx-8 hover:scale-110">Contact</Button>
  </div>
</nav>
