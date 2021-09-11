<script>
import { defineComponent } from 'vue'
import YouTube from 'vue3-youtube'

export default defineComponent({
  components: { YouTube },
})
</script>

<template>
  <div class="main h-full w-full flex content-center flex-col">
    <YouTube
      ref="youtube"
      class="absolute z-1 w-auto min-w-full min-h-full max-w-none"
      src="https://youtu.be/H0seL1bAoHg"
      :vars="{rel: 0, controls: 0, modestbranding: 1, autoplay: 1, loop: 1}"
      @ready="onReady"
    />
    <div class="absolute z-2 top-15 text-warm-gray w-full">
      <p class="text-4xl">
        <carbon-campsite class="inline-block" />
      </p>
      <p>
        The website is temporarily unavailable.
      </p>
      <p>
        <a class="m-3 text-sm btn bg-dark" rel="noreferrer" href="mailto:gordonfernblick@gmail.com" target="_blank">
          Contact us.
        </a>
      </p>
    </div>
  </div>
</template>

<style scoped>
.main {
  background: url('https://res.cloudinary.com/ahoy/image/upload/c_scale,w_1800/v1631014548/fernblick/1.webp');
  background-size: cover;
  background-position: center;
}
</style>
