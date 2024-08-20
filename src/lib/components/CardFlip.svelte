<script lang="ts">
  export let project: {
    title: string;
    description: string;
    imageUrl: string;
    link: string;
  };
</script>


<div class="mt-20 w-[18.75rem] h-[24rem] bg-transparent cursor-pointer group perspective">
  <div class="relative preserve-3d group-hover:my-rotate-y-180 w-full h-full duration-1000">
    <div class="absolute backface-hidden border-8 w-full h-full" style="border-color: #A3BFFA;">
      <img src={project.imageUrl} alt={project.title} class="w-full h-full" />
    </div>
    <div class="absolute my-rotate-y-180 backface-hidden w-full h-full bg-gray-100 overflow-hidden">
      <div class="text-center flex flex-col items-center justify-center h-full text-gray-800 px-[0.125rem] pb-[1.5rem]">
        <h1 class="text-3xl font-semibold pb-5">{project.title}</h1>
        <p class="pb-20">{project.description}</p>
        <a href={project.link} target="_blank" class="bg-[#a3bffa] px-[0.375rem] py-[0.125rem] font-semibold text-white rounded-full absolute translate-y-[0.4375rem] -bottom-[1rem] delay-500 duration-1000 group-hover:bottom-[5rem] scale-0 group-hover:scale-125">
          Try It Now!
        </a>
      </div>
    </div>
  </div>
</div>