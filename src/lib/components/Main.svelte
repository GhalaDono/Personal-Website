<script lang="ts">
  import CardFlip from "./CardFlip.svelte";
</script>

<main class="h-screen px-6 flex flex-col flex-1 p-4">
  <section
    id="introPage"
    class=" grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="text-[#A3BFFA] shadow-highlight">Ghala</span>
        Al-Masoudi
        <br />
        <span class="text-[#A3BFFA] shadow-highlight">Front-End</span>
        Developer
        <span class="text-sm floating-text">🫡 إن شاء الله</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl poppins">
        I am a student at Umm Al-Qura University, studying in the Faculty of
        Computing with a major in Computer Science, and I am a beginner in
        front-end development.
      </p>
      <a
        href="./contact"
        rel="noopener noreferrer"
        class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-blue-300 opacity-20 group-hover:translate-x-full z-0 duration-200"
        />
        <h4 class="relative z-9 font-bold">Get in touch &rarr;</h4>
      </a>
    </div>
    <!-- <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/profile.png"}
                alt="Zetane Engine"
                class="object-cover z-[2] max-h-[70vh]"
            />
        </div> -->
    <!-- <div  class="flex p-0.5 relative max-w-[700px] w-full mx-auto">
            <div
                class="absolute inset-0 overflow-hidden rounded-md flex items-center justify-center"
            >
                <div
                    class="bg-gradient-to-r absolute inset-[-20px]  from-violet-800 to-indigo-800 specialSpin"
                />
            </div>

            <img
                src={"images/zetane-engine.jpeg"}
                alt="Zetane Engine"
                class="w-full h-full object-cover z-[2]"
            />
        </div> -->
  </section>

  <section class="py-60 lg:py-96 flex flex-col lg:flex-row justify-center items-center gap-x-16 text-white">
    <div class="flex flex-col gap-2 text-center ">
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Here's my <span class="text-[#A3BFFA] shadow-highlight">projects</span>
      </h3>
      <div class="flex flex-wrap justify-center gap-10  mt-20">
        <div class=" sm:w-[15.625rem] md:w-[18.75rem] lg:w-[21.875rem] h-[26.25rem]">
          <CardFlip />
        </div>
        <div class=" sm:w-[15.625rem] md:w-[18.75rem] lg:w-[21.875rem] h-[26.25rem]">
          <CardFlip />
        </div>
      </div>      
    </div>
  </section>
        </main>