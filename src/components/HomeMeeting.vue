<template>
  <section>
    <div class="meeting is-wrap">
      <div class="meeting is-title">
        <div class="title is-line"><h2>Wanna find out who you are?</h2></div>
      </div>
      <div class="meeting is-content">
        <video
          autoplay
          muted
          loop
          playsinline
          ref="videoEl"
          :style="{ clipPath: `circle(${clipPathRadius}%)` }"
        >
          <source src="@/assets/hero.mp4" type="video/mp4" />
          Your browser does not support the video tag.
        </video>
        <div class="meeting is-cta">Book a meeting</div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const videoEl = ref(null);
const clipPathRadius = ref(5);

const handleScroll = () => {
  const scrollY = window.scrollY;
  const meetingSection = document.querySelector('.meeting.is-wrap');
  
  if (meetingSection) {
    const sectionTop = meetingSection.offsetTop;
    const sectionHeight = meetingSection.offsetHeight; // 300vh
    const scrollInSection = scrollY - sectionTop;
    
    if (scrollInSection >= 0 && scrollInSection <= sectionHeight) {
      // Calculate progress through the 300vh section (0 to 1)
      const progress = scrollInSection / sectionHeight;
      // Map progress to clip-path radius (5% to 100%)
      const radius = 5 + (progress * 95);
      clipPathRadius.value = Math.min(Math.max(radius, 5), 100);
    }
  }
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<style scoped>
video {
    clip-path: circle(5%);
    width: 100vw;
    height: 100vh;
    object-fit: cover;
}
</style>