<template>
  <div class="relative w-full min-h-screen overflow-hidden bg-[#020420]">
    <!-- Animated waves -->
    <div class="absolute inset-0 overflow-hidden">
      <svg class="waves" viewBox="0 24 150 28" preserveAspectRatio="none">
        <defs>
          <path id="wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z" />
        </defs>
        <g class="wave-parallax">
          <use href="#wave" x="48" y="0" fill="rgba(0,220,130,0.05)" />
          <use href="#wave" x="48" y="3" fill="rgba(0,220,130,0.04)" />
          <use href="#wave" x="48" y="5" fill="rgba(0,220,130,0.03)" />
          <use href="#wave" x="48" y="7" fill="rgba(0,220,130,0.02)" />
        </g>
      </svg>
    </div>

    <!-- Content -->
    <div class="relative z-10 flex flex-col items-center justify-center min-h-screen px-4 sm:px-6 lg:px-8 py-20">
      <!-- Version pill -->
      <a 
        href="#"
        class="mb-12 inline-flex items-center px-4 py-1.5 rounded-full text-sm font-medium bg-[#00DC8220] text-[#00DC82] hover:bg-[#00DC8230] transition-colors"
      >
        Nuxt v3.14 is out →
      </a>

      <!-- Main heading -->
      <h1 class="text-center max-w-4xl mx-auto">
        <span class="block text-4xl font-bold text-white sm:text-5xl lg:text-6xl mb-4">
          The Intuitive
        </span>
        <span class="block text-4xl font-bold text-[#00DC82] sm:text-5xl lg:text-6xl">
          Vue Framework
        </span>
      </h1>

      <!-- Description -->
      <p class="mt-6 text-lg sm:text-xl text-gray-400 max-w-3xl text-center leading-relaxed">
        Nuxt is an open source framework that makes web development intuitive and powerful.
        Create performant and production-grade full-stack web apps and websites with confidence.
      </p>

      <!-- Action buttons -->
      <div class="mt-10 flex flex-col sm:flex-row gap-4 justify-center items-center">
        <a
          href="#"
          class="px-6 py-3 rounded-lg bg-[#00DC82] text-black font-medium hover:bg-[#00DC82]/90 transition-colors"
        >
          Get Started →
        </a>
        <a
          href="#"
          class="px-6 py-3 rounded-lg text-white font-medium flex items-center gap-2 hover:bg-white/5 transition-colors"
        >
          <span>Nuxt in 100 Seconds</span>
          <div class="w-5 h-5 rounded-full border-2 flex items-center justify-center">
            <div class="w-2 h-2 border-l-2 border-t-2 rotate-45 translate-y-0.5 -translate-x-0.5"></div>
          </div>
        </a>
      </div>

      <!-- Terminal -->
      <div class="mt-10 w-full max-w-xl mx-auto">
        <div class="bg-[#1F2937] rounded-lg p-4 font-mono text-sm text-white/90">
          <div class="flex items-center">
            <span class="text-[#00DC82]">npx</span>
            <span class="ml-2">nuxi@latest init &lt;my-app&gt;</span>
            <button class="ml-auto hover:text-white" aria-label="Copy command">
              <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect>
                <path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"></path>
              </svg>
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.waves {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 100vh;
  margin-bottom: -7px;
  min-height: 100px;
  max-height: 150px;
}

.wave-parallax > use {
  animation: move-forever 25s cubic-bezier(.55,.5,.45,.5) infinite;
}
.wave-parallax > use:nth-child(1) { animation-delay: -2s; animation-duration: 7s; }
.wave-parallax > use:nth-child(2) { animation-delay: -3s; animation-duration: 10s; }
.wave-parallax > use:nth-child(3) { animation-delay: -4s; animation-duration: 13s; }
.wave-parallax > use:nth-child(4) { animation-delay: -5s; animation-duration: 20s; }

@keyframes move-forever {
  0% { transform: translate3d(-90px,0,0); }
  100% { transform: translate3d(85px,0,0); }
}

h1 {
  line-height: 1.1;
  letter-spacing: -0.03em;
}
</style>