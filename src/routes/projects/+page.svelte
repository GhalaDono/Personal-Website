<script lang="ts">
    import { onMount } from 'svelte';
    import Swiper from 'swiper';
    import 'swiper/swiper-bundle.css';

    
    onMount(() => {
        var swiper = new Swiper(".swiper", {
            grabCursor: true,
            initialSlide: 4,
            centeredSlides: true,
            slidesPerView: "auto",
            spaceBetween: 10,
            speed: 1000,
            freeMode: false,
            mousewheel: {
                thresholdDelta: 30
            },
            pagination: {
                el: ".swiper-pagination",
                clickable: true,
            },
        });

    });
</script>

<section  id="projects">
    <div class="flex flex-col gap-2 text-center">
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Here's my <span class="text-[#A3BFFA] shadow-highlight">projects</span>
        </h3>
    </div>
</section>

<div class="container py-10">
    <div class="swiper">
        <div class="swiper-wrapper">
            <div class="swiper-slide">
                <img src="pic/Calculator.png" alt="Calculator" />
                <p>Calculator</p>
            </div>
            <div class="swiper-slide">
                <img src="pic/ToDoList.png" alt="To Do List" />
                <p>To do list (Isn't completed)</p>
            </div>
        </div>
        <div class="swiper-pagination"></div>
    </div>
</div>
