<template>
  <section>
    <vueper-slides fractions progress lazy lazy-load-on-drag > <!-- TODO: add autoplay -->
      <vueper-slide
        v-for="(slide, i) in slides"
        :key="i"
        :image="slide.image"
        :title="slide.title"
        :content="slide.content"
        :link="slide.link"
      />
      <template #pause>
        <i class="icon pause_circle_outline"></i>
      </template>
    </vueper-slides>
  </section>
</template>

<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";

export default {
  components: { VueperSlides, VueperSlide },
  data: () => ({
    pauseOnHover: true,
    autoPlaying: true,
    internalAutoPlaying: true,
    slides: [
      {
        title: "El Teide Volcano, Spain",
        content: "Photo by Max Rive",
        image: require("@/assets/img-1.jpg"),
        link:
          "https://www.maxrivephotography.com/index/C0000rU1RKCHdqwI/G0000X57AtIzuRX0/I0000Gvr9HqdtyXk",
      },
      {
        title: "El Teide Volcano, Spain",
        content: "Photo by Max Rive",
        // You can also provide a URL for the image.
        image: require("@/assets/img-2.jpg"),
        link:
          "https://www.maxrivephotography.com/index/C0000rU1RKCHdqwI/G0000X57AtIzuRX0/I0000Gvr9HqdtyXk",
      },
    ],
  }),
};
</script>

<style lang="scss">
.vueperslide {
  background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);

  &:not(.no-shadow):not(.vueperslides--3d) &__parallax-wrapper {
    &:before, &:after {
      content: "";
      position: absolute;
      bottom: 100%;
      left: -1em;
      right: -1em;
      height: 2em;
      box-shadow: 0 0 20px rgba(#000, 0.25);
      z-index: 2;
    }

    &:after {
      top: 100%;
      bottom: auto;
    }
  }

  &__title {
    font-size: 7em;
    opacity: 0.6;
  }
}

.vueperslides__progress {
  background: rgba(0, 0, 0, 0.25);
}

/* If you want to hide the slide description while loading. */
.vueperslide--loading .vueperslide__content-wrapper {
  display: none !important;
}

</style>
