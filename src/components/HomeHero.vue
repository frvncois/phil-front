<template>
  <div class="hero is-wrap">
    <div class="hero is-overlay" :style="{ backdropFilter: `blur(${overlayBlur}em)` }"></div>
    <video
      autoplay
      muted
      loop
      playsinline
      ref="videoEl"
      :style="{ opacity: videoOpacity }"
    >
      <source src="@/assets/hero.mp4" type="video/mp4" />
      Your browser does not support the video tag.
    </video>
    <div class="hero is-content">
      <img src="@/assets/hero.svg">
      <div class="title is-line"><span>And you,</span></div>
      <div class="title is-line"><span>are business who can't</span></div>
      <div class="title is-line"><span>afford to be ignored.</span></div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const videoEl = ref(null);
const overlayBlur = ref(0);
const videoOpacity = ref(1);

const handleScroll = () => {
  const scrollY = window.scrollY;
  
  // Start blurring at 0vh, fully blurred at 75vh
  const blurAmount = Math.min((scrollY / (window.innerHeight * 0.75)) * 4, 4);
  overlayBlur.value = blurAmount;
  
  // Video opacity: starts fading at 100vh, fully transparent at 150vh
  const fadeStart = window.innerHeight; // 100vh
  const fadeEnd = window.innerHeight * 1.5; // 150vh
  
  if (scrollY <= fadeStart) {
    videoOpacity.value = 1;
  } else if (scrollY >= fadeEnd) {
    videoOpacity.value = 0;
  } else {
    const fadeProgress = (scrollY - fadeStart) / (fadeEnd - fadeStart);
    videoOpacity.value = 1 - fadeProgress;
  }
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});

const playFullscreen = () => {
  if (videoEl.value.requestFullscreen) {
    videoEl.value.requestFullscreen();
    videoEl.value.play();
  }
};
</script>
<style scoped>
video {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  z-index: -1;
}
</style>