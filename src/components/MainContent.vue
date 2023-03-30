<template>
  <div>
    <div class="banner">
      <div
        v-for="(image, index) in images"
        :key="index"
        :style="{ backgroundImage: 'url(' + image + ')' }"
        :class="{ 'image-active': activeImage === index }"
        class="image"
      ></div>
      <div class="title">
        <p class="title-text">{{ imageTitles[activeImage] }}</p>
      </div>
    </div>
    <div class="possibility">
      <div class="card card-1"></div>
      <div class="card card-2"></div>
      <div class="card card-3"></div>
    </div>
  </div>
</template>
<script>
export default {
  name: "MainContent",
  data() {
    return {
      activeImage: 0,
      images: [
        "https://lh3.googleusercontent.com/p/AF1QipM7rC9myfSv-UmZOE3ofNn0IvAPjyu1Nlvqb8PM=s1360-w1360-h1020",
        "https://lh5.googleusercontent.com/p/AF1QipNzZ78Eg9Vgi_-28rZD_Z-XjaPSO7o7Ux1dHpFs=s1455-k-no",
        "https://lh5.googleusercontent.com/p/AF1QipP8mm_bUt1LVxzquyT6w3JHMI2cl1Mya8STQWiw=s1941-k-no",
      ],
      imageTitles: [
        "Produit d'Asie",
        "Ramen variés",
        "Venez déguster nos Ramen!",
      ],
    };
  },
  created() {
    this.startAutoSlide();
  },
  methods: {
    startAutoSlide() {
      setInterval(() => {
        this.nextImage();
      }, 5000);
    },
    nextImage() {
      this.activeImage = (this.activeImage + 1) % this.images.length;
    },
  },
};
</script>
<style>
.banner {
  width: 100vw !important;
  height: 100vh;
  position: relative;
  overflow: hidden;
}

body {
  background: #e2e1e0;
  text-align: center;
}

.image {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-position: center center;
  background-size: cover;
  opacity: 0;
  transition: opacity 1s ease-in-out;
  filter: grayscale(0.2);
}

.image-active {
  opacity: 1;
}

.title {
  position: absolute;
  bottom: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.6);
  color: white;
  width: 100%;
  height: 15%;
  padding: 1rem;
  text-align: center;
  font-size: 1.5rem;
  font-weight: bold;
}

.title-text {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.possibility {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

@media only screen and (max-width: 600px) {
  .title {
    font-size: 1rem;
  }
}
</style>