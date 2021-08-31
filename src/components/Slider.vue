<template>
  <section>
    <vueper-slides fractions progress fixed-height="500px" slide-image-inside>
      <vueper-slide
        v-for="(slide, i) in slides"
        :key="i"
        :image="slide.image"
        :title="slide.title"
        :link="slide.link"
      />
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
        title: "Click on image to link",
        image:
          "https://www.regi.it/api/optimized-image/66fb5fdd6d48da2faaf66810064bc87f58ed3cc5071998085ce68d521413b295.jpg?&w=800&q=95",
        link:
          "https://www.regi.it/api/optimized-image/66fb5fdd6d48da2faaf66810064bc87f58ed3cc5071998085ce68d521413b295.jpg?&w=800&q=95",
      },
      {
        title: "Click on image to link",
        image:
          "https://www.regi.it/api/optimized-image/4b31d22fa3bafa2ddbfce9f35051a539721607e2b74b6d5d022fa64df5881bd7.jpg?&w=800&q=95",
        link:
          "https://www.regi.it/api/optimized-image/4b31d22fa3bafa2ddbfce9f35051a539721607e2b74b6d5d022fa64df5881bd7.jpg?&w=800&q=95",
      },
      {
        title: "Click on image to link",
        image:
          "https://www.regi.it/api/optimized-image/690042e3ed1335c0ec58fc042f2c38becfb64baff174b6477edccf7d1e642333.jpg?&w=800&q=95",
        link:
          "https://www.regi.it/api/optimized-image/690042e3ed1335c0ec58fc042f2c38becfb64baff174b6477edccf7d1e642333.jpg?&w=800&q=95",
      },
      {
        title: "Click on image to link",
        image:
          "https://www.regi.it/api/optimized-image/dfa3ff221c8d8e4db433f00c86d5dfbfc7363570cbc89098248edc0fbebe9d05.jpg?&w=800&q=95",
        link:
          "https://www.regi.it/api/optimized-image/dfa3ff221c8d8e4db433f00c86d5dfbfc7363570cbc89098248edc0fbebe9d05.jpg?&w=800&q=95",
      },
      {
        title: "Click on image to link",
        image:
          "https://www.regi.it/api/optimized-image/175d96f33aba230e7c0426225dd313775747d83f5c461c8c447a11ed96793d4f.jpg?&w=800&q=95",
        link:
          "https://www.regi.it/api/optimized-image/175d96f33aba230e7c0426225dd313775747d83f5c461c8c447a11ed96793d4f.jpg?&w=800&q=95",
      },
      {
        title: "Click on image to link",
        image:
          "https://www.regi.it/api/optimized-image/575b2ad0f821bcbcf66811ae3e7b8117089e2227a187c8adaa78a76a6fa9c6c0.jpg?&w=800&q=95",
        link:
          "https://www.regi.it/api/optimized-image/575b2ad0f821bcbcf66811ae3e7b8117089e2227a187c8adaa78a76a6fa9c6c0.jpg?&w=800&q=95",
      },
      {
        title: "Click on image to link",
        image:
          "https://www.regi.it/api/optimized-image/aece5b0fc83cfb0afbe86d08cbca5092069a3fdc0d913ac820794be1f8ebfdfd.jpg?&w=800&q=95",
        link:
          "https://www.regi.it/api/optimized-image/aece5b0fc83cfb0afbe86d08cbca5092069a3fdc0d913ac820794be1f8ebfdfd.jpg?&w=800&q=95",
      },
      {
        title: "Click on image to link",
        image:
          "https://www.regi.it/api/optimized-image/dc22546ec1e01cd0d3ab7e667a3b9db755bf3d97a78e72f34d34fe42baa4730e.jpg?&w=800&q=95",
        link:
          "https://www.regi.it/api/optimized-image/dc22546ec1e01cd0d3ab7e667a3b9db755bf3d97a78e72f34d34fe42baa4730e.jpg?&w=800&q=95",
      },
    ],
  }),
};
</script>

<style lang="scss">
.vueperslide {
  background: rgba(0, 0, 0, 0.25);
  position: relative;

  &__title {
    font-size: 25px;
    position: absolute;
    left: 5%;
    right: 5%;
    opacity: 0.9;
    color: rgb(51, 54, 56);
    white-space: none;
  }

  &__image {
    opacity: 0.4;
  }
}

.vueperslides {
  &__progress {
    background: rgba(0, 0, 0, 0.25);
    color: #ff5252;
  }

  &--fixed-height {
    height: 500px;
  }
}

@media screen and (max-width: 400px) {
  .vueperslide__title {
    font-size: 15px;
  }
}
</style>
