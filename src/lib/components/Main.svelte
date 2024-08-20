<script lang="ts">
  import CardFlip from "./CardFlip.svelte";

  const projects = [
    {
      title: "Calculator",
      description:
        "The \"Calculator\" project, built with Tailwind CSS and SvelteKit, is a responsive web app for simple arithmetic operations, focusing on seamless user experience and effective front-end interaction.",
        imageUrl:"./pic/Calculator.png",
        link:"https://ghaladono.github.io/Calculator/",
    },

    {
      title: "To-Do List",
      description:
        "The \"To-Do List\" project, built with Tailwind CSS and SvelteKit, is a web app for managing tasks with a responsive design and smooth performance. It allows users to add, edit, delete, and organize tasks efficiently.",
        imageUrl:"./pic/Calculator.png",
        link:"https://ghaladono.github.io/Calculator/",
    }
  ];
</script>

<main class="h-screen px-6 flex flex-col flex-1 p-4">
  <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
    <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10 mt-12">
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="text-[#A3BFFA] shadow-highlight">Ghala</span> Al-Masoudi
        <br />
        <span class="text-[#A3BFFA] shadow-highlight">Front-End</span> Developer
        <span class="text-sm floating-text ">🫡 إن شاء الله</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl poppins mt-3 ">
        I am a student at Umm Al-Qura University, studying in the Faculty of Computing with a major in Computer Science, and I am a beginner in front-end development.
      </p>
      <a href="./contact" rel="noopener noreferrer" class="
       mt-3 blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer">
        <div class="absolute top-0 right-full w-full h-full bg-blue-300 opacity-20 group-hover:translate-x-full z-0 duration-200 " />
        <h4 class="relative z-9 font-bold">Get in touch &rarr;</h4>
      </a>
    </div>
  </section>

  <section class=" py-20 lg:py-44 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center ">
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Here's my <span class="text-[#A3BFFA] shadow-highlight">projects</span>
      </h3>
      <div class="flex flex-wrap justify-center gap-5">
        {#each projects as project}
          <div class="sm:w-[15.625rem] md:w-[18.75rem] lg:w-[21.875rem] h-[26.25rem]">
            <CardFlip project={project} />
          </div>
        {/each}
      </div>      
    </div>
  </section>
</main>